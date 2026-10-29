---

---

Human brain generally looks for pattern. Nash Equilibrium states that any extent of randomness in human works is not random at all. However, experts in any field, in any domain fails to articulate such expertise due to lack of cognitive understanding. And, due to lack of answer of how an expert pulls such tricks, any type of expertise seems unreachable for novices. That is why research was published named [Reverse‑engineering expert similarity judgments: evidence from chess tactics]() this year. This paper used chess as an evaluating tool for understanding how human expert naturally looks for winner in the board. 

![](/assests/revchess.png)

Historically, cognitive researchers such as Chase and Simon, 1973, talked about chunking theory. They said, "*experts do not possess a larger short-term memory than novices. Instead, they store information in **meaningful chunks**, allowing them to process and remember more information efficiently.*" They used chess experiment too. The job for the participants was to memorize a chess board and set it up again with the pieces from memory. They evaluated that the novice saw the pieces as individual object and pawns. But, the expert made up stories and fantasies around the chunk and made it effective with unique cognitive skill. But, this study had gap. Though they were convinced that experts uses chunk as a memory retrieval but chunking was not enough in this case. If there was a new situation, expert can also handle it. This is why, Gobet and Simon at 1996 introduced Template theory. Template is made up of chunks. The main idea was to see how experts utilize the working memory by offloading vast information. They saw that experts use formation of the board as his advantage and make decisions based on it. It was never the individual particles rather formation as a whole that not only has more advantage with similar patterns but also was able to create unique decisions from unique formations never seen before. But the paper we are discussing made contact with the static vs dynamic approach of the whole expertise system presented by the perceptual cognitive system.

> The difference from static vs dynamic solution is position vs tactical sequential move. 

![](/assests/revchess1.png)

Prior literature lacked the perspective of pure computational model between the static and dynamic solution when judging problem similarity. With this gap, any type of design such as software or entertainment industry or product for business cannot evaluate properly how cognitive evaluation occur in case of problem misalignment. The study at the end found that, using machine learning model with human reviewing, expert similarity judgment is almost entirely driven by the dynamic solution. This means that, human may look for pattern but they mostly make decisions based on tactical and temporal assessment. 

> Static evaluation may look for advantage (mostly safety and security), but dynamic evaluation looks for temporary sacrifice for long term gain. This generally has better advantage while trading. Even in relationship, a novice might chunk up the words of the other indifferently. An expert will look for context, find formation or situation, tonal adjustment and ultimately gain advantage with unique situational awareness and precise template choices. 
> 

## Mechanism

The experiment used a **4-step computational pipeline** to reverse-engineer and explain how chess experts make similarity judgments:
### **1. Candidate Retrieval (Filtering the Puzzles)**

- **Searching a Massive Database:** An algorithm (BM25) scanned a database of **4.9 million chess puzzles** from Lichess.
- **Generating Pairs:** For each starting puzzle (query), the search engine retrieved **9 candidate puzzles** that already shared baseline similarities, filtering millions of options down to a focused set of comparison pairs.

### **2. Expert Annotation (Human Labeling)**

- **Solving & Evaluating:** A competitive chess expert solved each query puzzle on Lichess and replayed candidate solutions through a custom web application.
- **Binary Judgments:** She evaluated **324 query positions** (producing **2,866 total puzzle pairs**) and gave a simple binary label—**"similar"** or **"different"**—based on whether both puzzles reinforced the same tactical concept.
- **Cross-Expert Validation:** Two additional titled players (a FIDE Master and a Woman Grandmaster) evaluated a sample of puzzles to confirm that these similarity judgments were shared across experts rather than personal preference.

### **3. Machine Learning & Feature Extraction (Decoding the Criteria)**

- **Extracting Features:** For every puzzle pair, researchers generated **1,123 numeric features**, categorized into **static features** (board appearance, piece placements, pawn structures) and **dynamic features** (move sequences, sacrifices, checkmates).
- **Training Classifiers:** They trained interpretable machine learning models (such as ExtraTrees and decision trees) on the expert's labels to predict similarity decisions and reveal which features drove those decisions.

### **4. Qualitative Re-Evaluation (Closing the Loop)**

- **Reviewing Disputed Cases:** The researchers selected **30 puzzle pairs** where the expert's label disagreed with the model's prediction and asked the expert to re-examine them without seeing the model's feature rankings.
- **Confirming the Rule:** The expert reversed **70% (21 out of 30)** of her initial choices, with every single reversal changing to align with the model's prediction. This proved that initial mislabelings were caused by superficial visual distractions, confirming her true judgment relied on solution mechanics.


## Feature Contrast Model
Psychologists debated whether humans judge similarity like spatial map or checklist. Amos Tversky proposed the feature contrast model where he compared two objects by adding up their shared features and subtracting their differing features. When the differing feature passes a subjective threshold, that alone works like a dealbreaker, lowering perceived similarity.  

![](/assests/revchess3.png)
## Evidence
### Ablation Study
Dynamic solution features achieved AUC of 0.9 approximately. On the contrary, the static features only has 0.554. After removing static feature completely, the overall performance dropped for 0.002. AUC or Area Under the Curve measures predictive accuracy where 0.5 is a guess and 1 is perfect. Using, 355 pairwise contrast features from the study only showed that the model was right 90 percent of the time. 

![](/assests/revchess2.png)
### Checkmate Decision
The checkmate was ranked using the feature contrast model with accuracy reading. Checkmate agreement ranked **#1** across all four interpretability methods used in the study (decision tree root split, Gini importance, permutation importance, and logistic regression coefficient of −2.0).

### Cross Experiment Agreement
A FIDE master and a woman grandmaster evaluated 98 query positions being in the blackbox, ambiguous from primary annotator. And the rates exceeded the chance baseline of 60%. 

### Re-Evaluation
The researcher selected 30 puzzle pairs where models prediction contradicted the experts initial label. Upon, blind examination, the expert reversed 21 of the original labels. The shifted label matched the model prediction 100%.

![](/assests/revchess5.png)
![](/assests/revchess4.png)
## Conclusion

In real world problem solving, experts evaluate whether two situations are alike based on how they will work out rather than what they like in surface. Expert organize thinking based on major diagnostic rule such as whether the medical case is benign vs malignant. Then the judgement comes with alignment to the goal. This can be used in EdTech platforms where students struggle with problem or master a concept, the system presents varied problems to test using different setups. When the expert re-examined puzzle pairs where her initial label clashed with the AI model's prediction, she changed her mind 70% of the time, with 100% of those reversals aligning with the AI model. This proves that even experienced human experts can be temporarily tricked by superficial visual resemblances. Machine learning models can act as a reliable "second opinion" to refocus experts on deep, functional logic.

## Sources
[Reverse‑engineering expert similarity judgments: evidence from chess tactics](https://doi.org/10.1186/s41235-026-00755-5)

