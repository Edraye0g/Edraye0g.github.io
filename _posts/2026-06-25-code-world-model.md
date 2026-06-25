---

---

Most ongoing research on Large Language Models (LLMs) playing games treats the model like an "intuitive player"—you ask it what move to make, and it pulls from its vast training data to pick what *seems* right. It's like asking a chess grandmaster to play blindfolded, relying purely on pattern recognition. This "LLM as policy" approach works... to a point. But strategic mastery often requires deep multi-step lookahead, the kind of methodical thinking that doesn't emerge from pattern-matching alone. Think about it: even the world's best human chess players calculate 10 moves ahead, not just react to the immediate board state.

This is where Google's DeepMind team takes a fascinating turn. Instead of asking "What should the LLM *do*?", they asked "What should the LLM *know*?" The result is a paper that fundamentally reframes how we should think about LLMs in game-playing contexts.

## The Core Idea: Code World Models

The researchers propose using LLMs not as direct decision-makers, but as *induction engines* that translate natural language game rules and trajectory data into formal, executable Python code. They call this the **Code World Model (CWM)**.

Think of it like this: instead of asking Gemini to pick your next chess move, you ask Gemini to *understand the rules of chess* well enough to write a Python program that simulates chess. Then, you hand that program to a classical planner like Monte Carlo Tree Search (MCTS) to do the actual strategic thinking. The LLM becomes the teacher, not the player.

A CWM isn't just one function—it's a whole toolbox:
- **State transition function**: "What happens when I move the bishop?"
- **Legal move enumeration**: "Which moves are actually allowed right now?"
- **Termination checks**: "Is the game over?"
- **Reward function**: "Who scored what?"
- **Observation function** (for imperfect info): "What can player X actually *see*?"

The beautiful part? If the CWM is correct, then as you give the planner more compute time, the agent's play approaches optimal. You're shifting the burden from "LLM must be smart" to "LLM must be accurate." This is a crucial distinction.

## Algorithm: The Three-Layer System

The HGF paper had its Layer 1/2/3 processing. This paper has its own layered architecture:

### Layer 1: The Factory (CWM Synthesis)

The LLM is given:
1. A **textual description** of the game rules
2. **Offline trajectory data** (what happened in sample games)

From this, it generates Python code matching the OpenSpiel API format. But here's the thing—single-shot code generation usually produces garbage. So they use **iterative refinement** (think of it as code debugging on steroids):
- They auto-generate **unit tests** from the trajectories
- Failed tests → stack traces fed back to the LLM → LLM writes better code → repeat
- Two refinement strategies: **Conversation mode** (serial chat) and **Tree Search mode** (maintaining multiple CWMs, using Thompson sampling to pick which to refine next)

### Layer 2: The Inference Engine (For Imperfect Information Games)

This is where things get spicy. In games like Poker, you can't see the opponent's cards—the game has **latent states**. But ISMCTS (Information Set MCTS) needs to estimate hidden states to plan properly.

The researchers had the LLM **synthesize inference functions**—essentially code that estimates what the hidden state probably is, given only what the agent has seen and done. They call this "inference as code."

Two approaches:
- **Hidden history inference**: Sample plausible action histories that could explain what you observed
- **Hidden state inference**: Directly sample hidden states

It's like the LLM is learning to read the opponent's mind through code.

### Layer 3: The Value Estimator

They also prompt the LLM to generate **value functions**—heuristic functions that estimate "how good is this state?" This speeds up MCTS because instead of running random rollouts to estimate a leaf node's value, the planner can just *ask* the value function.

## The Great "Algorithm Bake-Off"

Before deploying on real humans, the researchers ran their method against three opponents across 10 games:

**The Contenders:**
- **Random**: Baseline—picks random legal moves
- **GT-(IS)MCTS**: The heavyweight champion using *actual* ground truth game code (upper bound)
- **Gemini 2.5 Pro (as policy)**: The "thinking" LLM asked to play directly

**The Games (5 Perfect Info, 5 Imperfect Info):**
- Perfect: Tic-tac-toe, Connect Four, Backgammon, Gen. Tic-tac-toe (OOD), Gen. Chess (OOD)
- Imperfect: Leduc Poker, Bargaining, Gin Rummy, Quadranto (OOD), Hand of War (OOD)

### The Results: CWM-(IS)MCTS as the Undisputed Champ

Here's the scoreboard:

**Perfect Information Games:**
- Against GT-MCTS: Roughly tied—both are similarly excellent (the CWM is nearly perfect)
- Against Gemini 2.5 Pro: **Clean sweep**—CWM-MCTS wins across all 5 games

**Imperfect Information Games (Open Deck):**
- Beats or matches Gemini 2.5 Pro in **4 out of 5** games
- Hand of War is the only loss, though this should be interpreted as Gemini being particularly weak there

**Imperfect Information Games (Closed Deck):**
- This is the "hard mode" where the agent has NO access to hidden states, even in training
- Performance degrades somewhat, but CWM-ISMCTS still beats or matches Gemini 2.5 Pro in all games

The one sore thumb? **Gin Rummy**. It's a game with intricate multi-step procedural subroutines (knocking, laying off melds, calculating deadwood, checking for undercuts) that the LLM struggles to capture perfectly. Even with 500 LLM calls, training accuracy was only ~78% and inference accuracy ~54%. This highlights a key frontier: mastering games with complex procedural logic.

## The Novel Contributions: Mic-Drop Moments

1. **Shifting the Paradigm**: Moving from "LLM as policy" to "LLM as world model generator" is the big conceptual win. It leverages LLM strengths (understanding semantics) while offloading computation to classical planners.

2. **Inference as Code**: Asking the LLM to synthesize inference functions for imperfect information games is genuinely novel. It's like the LLM is learning to build a "mind-reading" module through code.

3. **Closed Deck Learning**: The ability to learn CWMs even when hidden states are never observed—only the agent's own observations and actions—is a genuinely new capability. Previous work assumed "post-hoc observability" of hidden states. This paper cracks the harder problem.

4. **Generalization to OOD Games**: The fact that their approach works on *novel* games (not in the LLM's training set) is huge for real-world applicability.

## The Findings in Brief

1. **The LLM-as-teacher paradigm works**: By shifting from "LLM must play" to "LLM must teach," we get agents that are more accurate, more verifiable, and more generalizable.

2. **Tree search refinement beats conversation**: The multi-hypothesis tree search approach converges faster and more reliably than serial conversation refinement.

3. **Value functions are situational**: They helped significantly in Generalized Tic-Tac-Toe and Bargaining, but weren't universally beneficial across all games.

4. **Gin Rummy is a nightmare**: The procedural complexity breaks even 500 LLM calls. This reveals a frontier for future work.

5. **Closed deck is viable but imperfect**: Learning without hidden state access degrades quality, but game-playing performance remains competitive.

## The Bottom Line

This paper doesn't just show that LLMs can play games better—it shows that **LLMs can be used to build better game-playing systems**. The CWM framework is elegant: leverage LLM semantic understanding for model induction, then let classical planning algorithms do what they do best (deep search).

## Reference
[Code World Models for General Game Playing](https://arxiv.org/abs/2510.04542)