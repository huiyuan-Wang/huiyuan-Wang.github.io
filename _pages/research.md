---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

<div class="research-page">
  <div class="research-intro">
    <p class="research-intro__eyebrow">Statistics under modern information constraints</p>
    <p class="research-intro__lead">Modern learning rarely has access to clean, fully labeled, centrally pooled data. Confounders are hidden, labels are imperfect, datasets are fragmented across institutions, model outputs are modified by humans, and observations often obey complex structural constraints.</p>
    <p>I develop statistical principles for recovering reliable information under these conditions. Across causal inference, distributed learning, and modern AI, I ask what remains identifiable, what information must be validated or communicated, and which procedures are statistically optimal.</p>
    <p>My broader interests center on how learning systems acquire, retrieve, evaluate, and retain information. This includes active learning for data-efficient supervision, retrieval-augmented methods for grounding models in external evidence, statistically principled benchmarking and evaluation of large language models, continual learning under evolving tasks, and learning-system design that avoids shortcut solutions and improves out-of-distribution reliability.</p>
  </div>

  <div class="research-questions" aria-label="Questions guiding my research">
    <div><strong>What remains identifiable?</strong><span>Find the signal that survives hidden bias, indirect measurement, and structural constraints.</span></div>
    <div><strong>What information should move?</strong><span>Design summaries that preserve inferential value when raw data cannot be pooled.</span></div>
    <div><strong>What remains reliable?</strong><span>Build guarantees that hold as models, environments, and human behavior change.</span></div>
  </div>

  <section class="research-area" aria-labelledby="imperfect-evidence">
    <div class="research-area__heading">
      <span class="research-area__index" aria-hidden="true">01</span>
      <div>
        <h2 id="imperfect-evidence">Reliable Inference from Imperfect Evidence</h2>
        <p class="research-area__tagline">Causal inference, real-world evidence, and surrogate-powered inference</p>
      </div>
    </div>
    <p class="research-area__question">Can reliable conclusions be recovered when the variables we need are hidden and the labels we use may be wrong?</p>
    <div class="research-area__description">
      <p>My work turns auxiliary information into calibrated evidence. I use historical and negative controls to expose residual confounding, and flexible tree-based methods to learn heterogeneous treatment effects when standard identifying assumptions may fail. More recently, I have extended this perspective to surrogate-powered inference, combining abundant but noisy labels with limited high-quality validation data through regularization and adaptive labeling.</p>
      <p>The unifying goal is to make hidden bias and imperfect labels empirically diagnosable, correctable, and useful for inference&mdash;rather than simply assuming them away.</p>
    </div>
    <div class="research-area__outlook"><strong>Current directions</strong><span>Foundation-model outputs as surrogates; multimodal negative controls; adaptive validation; and principled integration of randomized trials with real-world evidence.</span></div>
    <h3>Selected work</h3>
    <ul class="research-paper-list">
      <li>
        <div class="research-paper__body"><a href="https://www.nature.com/articles/s41746-025-01821-w">Negative-Control-Calibrated Difference-in-Difference Analyses <span aria-hidden="true">&nearr;</span></a><p>Uses pre- and post-intervention negative controls to detect and adjust for time-varying unmeasured confounding, while remaining robust to partially unreliable controls.</p></div>
        <small>NPJ Digital Medicine, 2025</small>
      </li>
      <li>
        <div class="research-paper__body"><a href="https://proceedings.mlr.press/v202/tang23j.html">Difference-in-Differences Meets Tree-Based Methods <span aria-hidden="true">&nearr;</span></a><p>Learns heterogeneous treatment effects with a splitting rule that balances observed-data fit against violations of conditional parallel trends.</p></div>
        <small>ICML, 2023</small>
      </li>
      <li>
        <div class="research-paper__body"><a href="https://proceedings.neurips.cc/paper_files/paper/2022/hash/2526d439030a3af95fc647dd20e9d049-Abstract-Conference.html">Debiased Causal Tree <span aria-hidden="true">&nearr;</span></a><p>Uses historical controls and confounding entropy to recover heterogeneous causal effects in the presence of unmeasured confounding.</p></div>
        <small>NeurIPS, 2022</small>
      </li>
      <li>
        <div class="research-paper__body"><a href="https://arxiv.org/abs/2512.21826">Surrogate-Powered Inference: Regularization and Adaptivity <span aria-hidden="true">&nearr;</span></a><p>Combines validated labels and imperfect surrogates, using regularization and adaptive multiwave labeling to improve efficiency without sacrificing validity.</p></div>
        <small>Preprint, 2025</small>
      </li>
    </ul>
  </section>

  <section class="research-area" aria-labelledby="collaborative-inference">
    <div class="research-area__heading">
      <span class="research-area__index" aria-hidden="true">02</span>
      <div>
        <h2 id="collaborative-inference">Collaborative Inference without Data Pooling</h2>
        <p class="research-area__tagline">Distributed inference, heterogeneous populations, and reusable statistical summaries</p>
      </div>
    </div>
    <p class="research-area__question">When data cannot move, what information should?</p>
    <div class="research-area__description">
      <p>I study how to retain the inferential value of pooled data when observations are distributed across institutions, heterogeneous across populations, or missing in incompatible blocks. My work first showed that more aggregation can hurt: the gain from larger samples must be balanced against bias from heterogeneity, and communication structure determines which sites should borrow from one another.</p>
      <p>My recent work shifts the focus from aggregating model parameters to sharing information-preserving statistical objects. Transfer functions can safely augment an internal study with blockwise-missing external data; distributed calibration can reproduce pooled-data treatment comparisons; and MOSAiC compresses entire local risk functions so that sites communicate once while supporting accurate, flexible downstream analyses.</p>
    </div>
    <div class="research-area__outlook"><strong>Current directions</strong><span>Reusable one-shot summaries; multimodal and blockwise-fragmented studies; federated foundation models; and statistically principled collaboration among distributed AI agents.</span></div>
    <h3>Selected work</h3>
    <ul class="research-paper-list">
      <li>
        <div class="research-paper__body"><a href="https://doi.org/10.1080/01621459.2026.2698025">MOSAiC: Multi-site One-Shot Aggregation of Compressed Risk Functions <span aria-hidden="true">&nearr;</span></a><p>Uses tensor-train compression to communicate local risk functions once, attaining pooled-like accuracy and enabling new submodel analyses without further site queries.</p></div>
        <small>JASA, 2026</small>
      </li>
      <li>
        <div class="research-paper__body"><a href="https://arxiv.org/abs/2508.16902">Efficient Semiparametric Inference for Distributed Data with Blockwise Missingness <span aria-hidden="true">&nearr;</span></a><p>Develops one-round, do-no-harm augmentation that can attain the semiparametric efficiency bound while scaling to many external sites.</p></div>
        <small>Preprint, 2025</small>
      </li>
      <li>
        <div class="research-paper__body"><a href="https://arxiv.org/abs/2509.23664">Collaborative Indirect Treatment Comparisons with Multiple Distributed Single-Arm Trials <span aria-hidden="true">&nearr;</span></a><p>Provides doubly robust, pooled-equivalent treatment comparisons across isolated single-arm trials using only two communication rounds.</p></div>
        <small>Preprint, 2025</small>
      </li>
      <li>
        <div class="research-paper__body"><a href="https://proceedings.mlr.press/v195/zhao23b.html">The Aggregation&ndash;Heterogeneity Trade-off in Federated Learning <span aria-hidden="true">&nearr;</span></a><p>Shows why more data can be harmful under heterogeneity and characterizes when selective, neighbor-based aggregation is minimax optimal.</p></div>
        <small>COLT, 2023</small>
      </li>
    </ul>
  </section>

  <section class="research-area" aria-labelledby="adaptive-verifiable-ai">
    <div class="research-area__heading">
      <span class="research-area__index" aria-hidden="true">03</span>
      <div>
        <h2 id="adaptive-verifiable-ai">Statistical Foundations for Adaptive and Verifiable AI</h2>
        <p class="research-area__tagline">Generalization, knowledge retention, and statistical content provenance</p>
      </div>
    </div>
    <p class="research-area__question">How can modern learning systems remain understandable and verifiable as models, tasks, and their outputs evolve?</p>
    <div class="research-area__description">
      <p>I use non-asymptotic theory and optimal testing to study the full lifecycle of modern learning systems. On the learning side, I investigate why overparameterized neural networks generalize and how continual-learning algorithms balance forward transfer against retention of earlier knowledge. On the verification side, our team formulates LLM watermarking as a statistical testing problem and derives detection rules with explicit efficiency and optimality guarantees.</p>
      <p>A recurring theme is that familiar methods can fail in modern regimes: classical bias&ndash;variance intuition can miss the benefit of overparameterization, standard regularizers can be suboptimal across tasks, and additive watermark detectors lose robustness when humans edit generated text. The theory reveals these failure mechanisms and points to better procedures.</p>
    </div>
    <div class="research-area__outlook"><strong>Current directions</strong><span>Active and data-efficient learning; retrieval-augmented and knowledge-grounded systems; statistically principled benchmarking and evaluation of large language models; continual learning and model adaptation; and learning-system design that avoids shortcut solutions.</span></div>
    <h3>Selected work</h3>
    <ul class="research-paper-list">
      <li>
        <div class="research-paper__body"><a href="https://doi.org/10.1093/jrsssb/qkaf056">Robust Detection of Watermarks for Large Language Models under Human Edits <span aria-hidden="true">&nearr;</span></a><p>Introduces an adaptive truncated goodness-of-fit detector that remains optimal under substantial edits, where common sum-based rules lose robustness.</p></div>
        <small>JRSS-B, 2026</small>
      </li>
      <li>
        <div class="research-paper__body"><a href="https://doi.org/10.1214/24-AOS2468">A Statistical Framework of Watermarks for Large Language Models <span aria-hidden="true">&nearr;</span></a><p>Connects pivots, false-negative efficiency, and minimax optimization to derive powerful and principled watermark detection rules.</p></div>
        <small>AoS, 2025</small>
      </li>
      <li>
        <div class="research-paper__body"><a href="https://proceedings.mlr.press/v235/zhao24n.html">A Statistical Theory of Regularization-Based Continual Learning <span aria-hidden="true">&nearr;</span></a><p>Characterizes the forward&ndash;backward transfer trade-off and derives regularization schemes that match the order of an all-data oracle.</p></div>
        <small>ICML, 2024</small>
      </li>
      <li>
        <div class="research-paper__body"><a href="https://arxiv.org/abs/2106.04795">Nonasymptotic Theory for Two-Layer Neural Networks <span aria-hidden="true">&nearr;</span></a><p>Uses a ridge&ndash;lasso duality to explain double descent and when overparameterized networks can outperform their underparameterized counterparts.</p></div>
        <small>Preprint</small>
      </li>
    </ul>
  </section>

  <section class="research-area" aria-labelledby="structure-dynamics">
    <div class="research-area__heading">
      <span class="research-area__index" aria-hidden="true">04</span>
      <div>
        <h2 id="structure-dynamics">Learning Structure and Dynamics from Complex Data</h2>
        <p class="research-area__tagline">Constrained geometry, dynamic graphs, and scientific machine learning</p>
      </div>
    </div>
    <p class="research-area__question">Can structure recover information that standard data representations appear to lose?</p>
    <div class="research-area__description">
      <p>I develop methods that use geometry, sparsity, and relational dynamics to reveal interactions hidden by nonstandard observations. CARE shows that although compositional measurements obscure absolute scale, sparsity and increasing dimension can restore identifiability: in sufficiently high dimensions, its precision-matrix estimator is minimax optimal and performs as if the latent basis were observed. Related work recovers nonlinear dependence graphs from asynchronous event streams and models out-of-distribution fluid dynamics through disentangled graph ODEs.</p>
      <p>This direction treats structure not as a complication to work around, but as information that can make otherwise difficult learning and inference problems solvable.</p>
    </div>
    <div class="research-area__outlook"><strong>Current directions</strong><span>Foundation models for structured and time-series data; scientific world models; causal discovery in complex systems; and multimodal scientific data with known structural constraints.</span></div>
    <h3>Selected work</h3>
    <ul class="research-paper-list">
      <li>
        <div class="research-paper__body"><a href="https://doi.org/10.1080/01621459.2024.2335586">CARE: Large Precision Matrix Estimation for Compositional Data <span aria-hidden="true">&nearr;</span></a><p>Reveals a blessing of dimensionality: high-dimensional sparsity restores identifiability and enables optimal network recovery from compositional observations.</p></div>
        <small>JASA, 2025</small>
      </li>
      <li>
        <div class="research-paper__body"><a href="https://openreview.net/forum?id=JsPvL6ExK8">Prometheus: Out-of-Distribution Fluid Dynamics Modeling with Disentangled Graph ODE <span aria-hidden="true">&nearr;</span></a><p>Separates invariant physical dynamics from environment-specific factors to improve out-of-distribution modeling of complex fluid systems.</p></div>
        <small>ICML, 2024</small>
      </li>
      <li>
        <div class="research-paper__body"><a href="https://arxiv.org/abs/2110.11562">Temporal Point Process Graphical Models <span aria-hidden="true">&nearr;</span></a><p>Recovers nonlinear temporal dependence structures from high-dimensional, asynchronous streams of events.</p></div>
        <small>Preprint</small>
      </li>
    </ul>
  </section>

</div>
