---
layout: page
title: "About & Portfolio"
permalink: /about/
---

<!-- Profile Hero Header -->
<div class="portfolio-hero">
  <div class="portfolio-avatar-wrapper">
    <img src="/assets/Al Mutakabbir,M. R.jpg" alt="Rayeed Al Mutakabbir" class="portfolio-avatar-img" onerror="this.style.display='none'; document.getElementById('avatar-fallback').style.display='flex';" />
  </div>
  <div class="portfolio-hero-info">
    <h1 class="portfolio-name">Rayeed Al Mutakabbir</h1>
    <div class="portfolio-role">Biomedical Engineering Undergraduate &amp; Bioinformatics Research Assistant</div>
    
    <div class="portfolio-status-pill">
      <span class="status-dot"></span>
      <span>Open for Graduate Research &amp; Academic Collaborations</span>
    </div>

    <div class="portfolio-socials">
      <a href="mailto:mutakabbirmra@gmail.com" class="social-btn">
        <span></span> Email
      </a>
      <a href="https://github.com/Edraye0g" target="_blank" rel="noopener noreferrer" class="social-btn">
        <span></span> GitHub
      </a>
      <a href="https://www.linkedin.com/in/rayeed-al-mutakabbir-24102315b/" target="_blank" rel="noopener noreferrer" class="social-btn">
      <span></span> LinkedIn
      </a>
      <a href="{{ "/posts" | relative_url }}" class="social-btn">
        <span></span> Reviews ({{ site.posts | size }})
      </a>
      <a href="{{ "/contact" | relative_url }}" class="social-btn">
        <span></span> Contact
      </a>
    </div>
  </div>
</div>

<!-- Biography / Statement -->
<h2 class="portfolio-section-heading"><span>🔬</span> Research Statement &amp; Biography</h2>

<p>
  I am a Biomedical Engineering undergraduate at <strong>Khulna University of Engineering &amp; Technology (KUET)</strong> with a strong focus on <strong>Computational Psychiatry</strong>, <strong>Cognitive Neuroscience</strong>, and <strong>Neuroimaging</strong>.
</p>

<p>
  My research focuses on understanding <em>how the human brain navigates uncertainty, forms beliefs, and makes decisions</em>. By combining principles from <strong>Bayesian inference</strong>, <strong>functional near-infrared spectroscopy (fNIRS)</strong>, and <strong>electrophysiological signal analysis (EEG)</strong>, I investigate the physiological and computational mechanisms underlying cognitive biases, stress responses, and mental health dysfunctions.
</p>

<p>
  Through this blog, I write comprehensive literature reviews of recent landmark papers across neuroscience, machine learning, and bioinformatics, translating theoretical research into clear computational and physiological models.
</p>

<!-- Primary Research Domains -->
<h2 class="portfolio-section-heading"><span>🧠</span> Primary Research Domains</h2>

<div class="portfolio-grid-2col">
  <div class="project-card">
    <h3>Computational Psychiatry</h3>
    <p>
      Modeling aberrant belief updating, cognitive distortions, and predictive processing failures using generative frameworks such as the Hierarchical Gaussian Filter (HGF) and active inference.
    </p>
    <div class="tag-cloud">
      <span class="badge badge-purple">Predictive Coding</span>
      <span class="badge badge-blue">Bayesian Brain</span>
      <span class="badge badge-yellow">HGF Models</span>
    </div>
  </div>

  <div class="project-card">
    <h3>Decision-Making Under Uncertainty</h3>
    <p>
      Analyzing value computation, subjective utility, ambiguity resolution, and the neural substrates governing social fairness, risk appraisal, and cognitive fatigue across prefrontal networks.
    </p>
    <div class="tag-cloud">
      <span class="badge badge-blue">Neuroeconomics</span>
      <span class="badge badge-purple">Utility Theory</span>
      <span class="badge badge-yellow">vmPFC &amp; TPJ</span>
    </div>
  </div>

  <div class="project-card">
    <h3>Neuroimaging &amp; Biosignal Processing</h3>
    <p>
      Developing signal processing pipelines for functional Near-Infrared Spectroscopy (fNIRS) and EEG, focusing on motion artifact reduction, hemodynamic response modeling, and time-frequency dynamics.
    </p>
    <div class="tag-cloud">
      <span class="badge badge-purple">fNIRS Hemodynamics</span>
      <span class="badge badge-blue">EEG Time-Frequency</span>
      <span class="badge badge-yellow">Artifact Removal</span>
    </div>
  </div>

  <div class="project-card">
    <h3>Bioinformatics &amp; Complex Systems</h3>
    <p>
      Investigating systemic complexity, information theory (maximum entropy), neural circuit connectivity graphs, and computational pipelines for cancer genomic sequence analysis.
    </p>
    <div class="tag-cloud">
      <span class="badge badge-blue">Cancer Genomics</span>
      <span class="badge badge-purple">Information Theory</span>
      <span class="badge badge-yellow">Graph Dynamics</span>
    </div>
  </div>
</div>

<!-- Research Experience -->
<h2 class="portfolio-section-heading"><span>💼</span> Research Experience</h2>

<div class="timeline-card">
  <div class="timeline-dot"></div>
  <div class="timeline-period">Feb 2026 – Present</div>
  <h3 class="timeline-title">Undergraduate Research Assistant in Bioinformatics</h3>
  <div class="timeline-place">Bioinformatics &amp; Computational Biology Research</div>
  <p>
    Conducting computational research at the intersection of genomics, statistical data science, and biomedical machine learning, with focused applications in cancer genomics.
  </p>
  
  <ul>
    <li><strong>Hands-on Machine Learning for Cancer Genomics:</strong> Built and trained supervised and unsupervised machine learning models on high-dimensional genomic datasets for molecular tumor subtyping, biomarker identification, and predictive feature modeling.</li>
    <li><strong>Statistical Analysis &amp; Data Science:</strong> Conducted comprehensive exploratory data analysis (EDA), hypothesis testing, normalization workflows, and differential gene expression analysis.</li>
    <li><strong>Scientific Data Illustration:</strong> Designed publication-grade scientific visualizations, including heatmaps, volcano plots, PCA/t-SNE dimensionality reduction plots, and biological pathway diagrams.</li>
    <li><strong>Research Paper Writing &amp; Collaboration:</strong> Actively contributed to academic manuscript drafting, background literature synthesis, results interpretation, and collaborative workflows in a multidisciplinary research team.</li>
  </ul>

  <div class="tag-cloud">
    <span class="badge badge-purple">Cancer Genomics</span>
    <span class="badge badge-blue">Hands-on Machine Learning</span>
    <span class="badge badge-yellow">Statistical Analysis</span>
    <span class="badge badge-purple">Data Illustration</span>
    <span class="badge badge-blue">Research Paper Writing</span>
    <span class="badge badge-yellow">Collaborative Research</span>
  </div>
</div>

<!-- Featured Projects -->
<h2 class="portfolio-section-heading"><span>⚙️</span> Featured Projects &amp; Engineering Work</h2>

<div class="portfolio-grid-2col">
  <div class="project-card">
    <h3>fNIRS Motion Artifact Correction &amp; Hemodynamic Processing</h3>
    <p>
      Engineered analytical filtering workflows for functional Near-Infrared Spectroscopy (fNIRS) data acquired over the prefrontal cortex. Implemented wavelet-based motion artifact removal, baseline drift reduction, and modified Beer-Lambert law transformations to extract oxygenated and deoxygenated hemoglobin ($\Delta\text{HbO}$, $\Delta\text{HbR}$) metrics.
    </p>
    <div class="tag-cloud">
      <span class="badge badge-blue">Python</span>
      <span class="badge badge-purple">SciPy</span>
      <span class="badge badge-yellow">Optical Imaging</span>
      <span class="badge badge-blue">Wavelet Filtering</span>
    </div>
  </div>

  <div class="project-card">
    <h3>EEG Panic-Like Stress Severity Detection</h3>
    <p>
      Designed an electrophysiological data analysis pipeline to detect acute panic-like stress severity. Extracted band powers (Delta, Theta, Alpha, Beta) and spectral entropy from multi-channel EEG recordings, correlating fronto-cortical asymmetry with autonomic nervous system reactivity.
    </p>
    <div class="tag-cloud">
      <span class="badge badge-purple">EEG Processing</span>
      <span class="badge badge-yellow">Spectral Entropy</span>
      <span class="badge badge-blue">Biosignal Analysis</span>
      <span class="badge badge-purple">Python</span>
    </div>
  </div>

  <div class="project-card">
    <h3>Photoplethysmography (PPG) Real-Time Metric Pipeline</h3>
    <p>
      Constructed a pulse oximetry and finger photoplethysmography processing system. Designed adaptive threshold peak-detection algorithms to compute instantaneous pulse rate, pulse arrival time, and heart rate variability (HRV) time-domain indicators under baseline and stress conditions.
    </p>
    <div class="tag-cloud">
      <span class="badge badge-yellow">Pulse Oximetry</span>
      <span class="badge badge-blue">Heart Rate Variability</span>
      <span class="badge badge-purple">Peak Detection</span>
      <span class="badge badge-blue">MATLAB / Python</span>
    </div>
  </div>

  <div class="project-card">
    <h3>Compendium of Academic Reviews (25+ Publications)</h3>
    <p>
      Authored extensive, mathematically rigorous critiques analyzing recent peer-reviewed literature across computational neurobiology, economic decision-making, Bayesian learning, and linguistics. Each article translates dense experimental paradigms into conceptual clarity.
    </p>
    <div class="tag-cloud">
      <span class="badge badge-purple">Scientific Writing</span>
      <span class="badge badge-blue">Computational Modeling</span>
      <span class="badge badge-yellow">Literature Critique</span>
    </div>
  </div>
</div>

<!-- Technical Toolset -->
<h2 class="portfolio-section-heading"><span>🛠️</span> Technical Skills &amp; Methodologies</h2>

<div class="skills-category-box">
  <h4>Programming &amp; Quantitative Computing</h4>
  <div class="tag-cloud">
    <span class="badge badge-blue">Python (NumPy, SciPy, Matplotlib, Pandas)</span>
    <span class="badge badge-purple">MATLAB / GNU Octave</span>
    <span class="badge badge-yellow">R</span>
    <span class="badge badge-blue">C / C++</span>
    <span class="badge badge-purple">Bash / Shell Scripting</span>
  </div>
</div>

<div class="skills-category-box">
  <h4>Neuroimaging &amp; Biosignal Analysis</h4>
  <div class="tag-cloud">
    <span class="badge badge-purple">fNIRS Hemodynamic Modeling</span>
    <span class="badge badge-blue">EEG Time-Frequency Decomposition</span>
    <span class="badge badge-yellow">HRV Autonomic Analysis</span>
    <span class="badge badge-purple">Wavelet &amp; FIR/IIR Filter Design</span>
    <span class="badge badge-blue">Artifact Subspace Removal</span>
  </div>
</div>

<div class="skills-category-box">
  <h4>Theoretical &amp; Computational Frameworks</h4>
  <div class="tag-cloud">
    <span class="badge badge-blue">Bayesian Inference</span>
    <span class="badge badge-purple">Hierarchical Gaussian Filter (HGF)</span>
    <span class="badge badge-yellow">Maximum Entropy Formulations</span>
    <span class="badge badge-blue">Markov Decision Processes</span>
    <span class="badge badge-purple">Information Theory</span>
  </div>
</div>

<div class="skills-category-box">
  <h4>Development &amp; Research Tools</h4>
  <div class="tag-cloud">
    <span class="badge badge-purple">Linux / WSL</span>
    <span class="badge badge-blue">Git &amp; GitHub</span>
    <span class="badge badge-yellow">LaTeX &amp; Overleaf</span>
    <span class="badge badge-purple">Jekyll &amp; Markdown</span>
    <span class="badge badge-blue">Jupyter Notebooks</span>
  </div>
</div>

<!-- Education Timeline -->
<h2 class="portfolio-section-heading"><span>🎓</span> Education &amp; Academic Background</h2>

<div class="timeline-card">
  <div class="timeline-dot"></div>
  <div class="timeline-period">Undergraduate Studies</div>
  <h3 class="timeline-title">Bachelor of Science in Biomedical Engineering (B.Sc. in BME)</h3>
  <div class="timeline-place">Khulna University of Engineering & Technology (KUET)</div>
  <div class="timeline-period">Oct 2023 – Present</div>
  <p>
    Rigorous training covering biomedical instrumentation, neural engineering, physiological control systems, biomedical signal processing, biomaterials, and medical imaging systems.
  </p>
</div>
<div class="timeline-card">
  <div class="timeline-dot"></div>
  <div class="timeline-period">Higher Secondary Education</div>
  <h3 class="timeline-title">HSC, Passed with GPA-5</h3>
  <div class="timeline-place">Saint Joseph Higher Secondary School, Asad Gate, Dhaka</div>
  <div class="timeline-period">2020-2022</div>
</div>
<div class="timeline-card">
  <div class="timeline-dot"></div>
  <div class="timeline-period">Secondary Education</div>
  <h3 class="timeline-title">SSC, Passed with GPA-5</h3>
  <div class="timeline-place">Ideal School and College, Motijhil, Dhaka</div>
  <div class="timeline-period">2016-2020</div>
</div>

<!-- Collaboration CTA -->
<div class="portfolio-cta-card">
  <h3 style="margin-top: 0; font-size: 1.5rem;">Let's Connect &amp; Collaborate</h3>
  <p style="color: var(--text-muted); max-width: 600px; margin: 0.5rem auto 1.5rem;">
    Interested in collaborating on computational neuroscience research, discussing literature, or sharing graduate study opportunities? I would love to connect.
  </p>
  <div style="display: flex; gap: 12px; justify-content: center; flex-wrap: wrap;">
    <a href="mailto:mutakabbirmra@gmail.com" class="social-btn primary-btn">
      Send an Email
    </a>
    <a href="https://github.com/Edraye0g" target="_blank" rel="noopener noreferrer" class="social-btn">
      View GitHub Profile
    </a>
    <a href="{{ "/contact" | relative_url }}" class="social-btn">
      Contact Page
    </a>
  </div>
</div>
