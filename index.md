---
layout: page
---

<div class="hero-banner">
  <span class="hero-badge">Computational Psychiatry & Neuroscience</span>
  <h1 class="hero-title">Literature Reviews & Neural Inquiries</h1>
  <p class="hero-subtitle">
    Deconstructing research on neural decision-making under uncertainty, probabilistic cognitive modeling, complex biological systems, and mental state dynamics.
  </p>
</div>

<h2 class="posts-section-title">Explore by Domain</h2>

<div class="category-grid">
  <a href="{{ "/neuroscience" | relative_url }}" class="category-card">
    <span class="category-icon">🧠</span>
    <h2>Neuroscience <span class="category-arrow">→</span></h2>
    <p>Exploring brain function, neural decision making, and cognitive mechanisms.</p>
  </a>

  <a href="{{ "/algorithm" | relative_url }}" class="category-card">
    <span class="category-icon">⚡</span>
    <h2>Algorithms <span class="category-arrow">→</span></h2>
    <p>Understanding computational modeling, Bayesian updates, and mathematical frameworks.</p>
  </a>

  <a href="{{ "/complex" | relative_url }}" class="category-card">
    <span class="category-icon">🕸️</span>
    <h2>Complex Science <span class="category-arrow">→</span></h2>
    <p>Investigating emergence, connectivity networks, and nonlinear dynamics.</p>
  </a>

  <a href="{{ "/bioinformatics" | relative_url }}" class="category-card">
    <span class="category-icon">🧬</span>
    <h2>Bioinformatics <span class="category-arrow">→</span></h2>
    <p>Computational approaches to biological sequence analysis and data science.</p>
  </a>

  <a href="{{ "/unhinged" | relative_url }}" class="category-card">
    <span class="category-icon">💭</span>
    <h2>Unhinged Thoughts <span class="category-arrow">→</span></h2>
    <p>Interdisciplinary hypotheses, mental models, and ideas that defy rigid categorizations.</p>
  </a>
</div>

<section class="recent-posts-section">
  <h2 class="posts-section-title">Latest Reviews</h2>
  <div class="post-preview-list">
    {% for post in site.posts limit:6 %}
    <article class="post-preview-card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="post-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
        {% if post.categories.first %}
        · <span class="post-category-tag" style="color: var(--accent-primary); font-weight: 500;">{{ post.categories.first | capitalize }}</span>
        {% endif %}
      </p>
    </article>
    {% endfor %}
  </div>
  <div style="margin-top: 1.5rem; text-align: right;">
    <a href="{{ "/posts" | relative_url }}" style="font-weight: 600; font-size: 1rem; color: var(--accent-primary);">
      View all {{ site.posts | size }} reviews & posts →
    </a>
  </div>
</section>
