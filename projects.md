[Home](index.md) | [Research](research.md) | [Projects & Awards](projects.md)

---

## Machine Learning & AI

### **Little Sparrow: Edge Wildlife Monitoring with Calibrated Bird Identification**
**Tech Stack:** Python, PyTorch, BioCLIP 2, YOLO11, SQLite  
**Deployment Target:** NVIDIA Jetson Orin Nano via ONNX/TensorRT

Developing a camera-and-microphone system that identifies bird feeder visitors and consolidates video detections into animal visits. The intended record resembles a naturalist’s notebook: a life list, and daily and seasonal activity.

- **Vision Pipeline:** Motion-gated detection combines YOLO11 boxes with supplementary motion regions. Small animal-type and bird-species classifiers share frozen BioCLIP 2 embeddings.
- **Calibrated Species Identification:** Temperature scaling and species-level abstention distinguish named birds from unsupported identifications. Photograph evaluations achieved 95% precision among named-species predictions.
- **Visit-Level Records:** Tracking consolidates detections into SQLite records containing images, predictions, confidence trajectories, human corrections, and model versions. These support ecological summaries and a reviewed dataset for future model updates.
- **Ongoing Development:** Visit-level audio corroboration for visually hard-to-distinguish bird pairs.

**Long-Term Goal:** Contribute reliable field observations to studies of seasonal occurrence and migration timing, supporting wildlife conservation.


### **Vincero Monopoly POMDP: Bayesian Simulation Engine**
**Tech Stack:** Python, NumPy, Gymnasium, Stable-Baselines3 (PPO)

A rules-exact Monopoly simulation built on a Partially Observable Markov Decision Process (POMDP) architecture. The core contribution is a **Monte Carlo win probability estimator** that answers: *Given the current board — each player's cash, properties, and buildings — what is each player's probability of winning?*

* **Win Probability Estimation:** Specify any board state (cash holdings, property ownership, building counts) for all players via the `ScenarioBuilder`, and the estimator rolls out hundreds of simulated games — sampling hidden deck permutations and latent opponent risk profiles — to produce P(win \| state) for each player. Parameter sweeps reveal how sensitive these probabilities are to changes in cash, position, or development.
* **POMDP Architecture:** Models Monopoly with genuine information asymmetry — hidden deck order and latent opponent aggressiveness (θ ∈ [0,1]) — rather than treating it as a fully observable optimization problem.
* **Key Findings:** First-mover advantage yields ~6 percentage points over the fair baseline of 25%; aggressive play consistently dominates conservative strategies; the game's tipping point — where one player's advantage becomes statistically irreversible — typically occurs around turns 80–120 when developed monopolies outpace GO salary.
* **RL Integration:** A Gymnasium-wrapped environment (246-dim observation, 90 discrete actions) supports PPO training via Stable-Baselines3 against heuristic opponents.

[View on GitHub](https://github.com/TrevorWrobleski/Vincero)

### **Project Argos: Bayesian Search Optimization**
**Tech Stack:** Python, NumPy, SciPy, Bayesian Model Averaging (BMA)

A Bayesian Model Averaging engine for optimal search under uncertainty. Fuses competing expert hypotheses into a coherent probability map and dynamically allocates search effort to maximize target detection.
* **Expert Fusion (BMA):** Implements M-open Bayesian Model Averaging (comparing multiplicative updating vs. log-score stacking) to dynamically weight expert priors based on accumulating search evidence.
* **Allocation Strategies:** Evaluates sequential posterior updating against multiple search policies, including Greedy, Re-search Aware, Entropy-Minimizing, and custom Adaptive thresholding.
* **Key Findings:** Demonstrates via Monte Carlo simulation that investing in prior quality strictly dominates allocation strategy optimization; equal-weight BMA successfully hedges against costly misdirection without sacrificing rapid detection times.

[View on GitHub](https://github.com/TrevorWrobleski/Argos)

---

## Applied Statistics & Modeling

### **Thoroughbred Asset Pricing Model**
**Focus:** Financial Modeling, Regression Analysis

Predictive modeling to estimate the value of Thoroughbred racehorses as financial assets. This project integrates pedigree, physical attributes, and market trends to model earning potential and cost structures across the animal's life stages.

### **Traumatic Brain Injury (TBI) Recovery Trajectories**
**Focus:** Survival Analysis, Time-Series Forecasting

Predictive modeling to assess recovery paths for TBI patients. Integrates patient-specific covariates and therapy progress data to support clinical decision-making. Currently benchmarking Random Forests and Gradient Boosting Machines against Recurrent Neural Networks (RNNs).

---

## Software & Research Tools

### **ToxBase: Open-Source Platform for Standardized Toxicology Data**
**Tech Stack:** Python, Flask, SQLAlchemy, SQL

A web application addressing data fragmentation in toxicology. ToxBase implements a hierarchical data model (Study → Animal Model → Dose Group → Outcome) to standardize disparate formats.
* **Features:** Controlled vocabularies for dose units/routes and a dynamic metadata system for custom fields.
* **Impact:** Facilitates cross-study comparisons for regulatory submissions and enables robust meta-analyses for benchmark dose estimation.
* **Research Relevance:** Directly supports my work in Bayesian prior elicitation by providing high-quality, structured data.

[View on GitHub](https://github.com/TrevorWrobleski/ToxBase)

### **Rexicon: Offline English–Mandarin Transcription and Translation**

**Tech Stack:** Python, Silero VAD, Whisper, MLX, faster-whisper/CTranslate2, Helsinki-NLP OPUS-MT, OpenCC, CustomTkinter

Built a desktop application to support human interpreters with live transcription, bidirectional translation, and domain-specific terminology references. Live microphone input and recorded audio are processed locally after initial model installation.

- **Streaming Recognition:** Silero VAD segments speech using duration-dependent pause thresholds and maximum-duration splits. Live previews distinguish provisional text from prefixes supported by agreement between successive Whisper hypotheses and a timestamp-based holdback.
- **Inference Scheduling:** Separate recognition and translation workers prioritize finalized utterances over previews. Backlog thresholds stop live capture while accepted phrases finish processing, rather than allowing latency to grow indefinitely.
- **Translation and Review:** Processes token-budgeted source chunks without input truncation. End-token checks, bounded retries, and explicit failure markers identify incomplete output. Glossary entries provide recognition hints and flag missing preferred translations without forcing substitutions.
- **Local Execution and Records:** Whisper runs through MLX on Apple silicon or CTranslate2 on CPU/CUDA. Session journals retain transcript revisions, warnings, processing times, and model settings.

[View Project Page](https://trevorwrobleski.github.io/rexicon_dev.github.io/)

### **Kentucky Derby Color Palettes**
**Tech Stack:** R, ggplot2

An R package offering visualization palettes inspired by the pageantry of the Kentucky Derby.
* **Design:** Includes qualitative, sequential, and diverging palettes drawn from jockey silks and Bluegrass landscapes.
* **Utility:** Features colorblind-safe options and a `derby_theme()` for publication-ready graphics.

[View on GitHub](https://github.com/TrevorWrobleski/kentuckyderby/)

---


## Awards and Recognition

**Academic Fellowships & Funding**
* **ESRC Doctoral Training Partnership Studentship** – Competitive funding for PhD research at LSE.
* **Bloomberg Fellow** – Selected for leadership potential and academic excellence in global affairs.
* **Gilman Scholarship** – Awarded for academic achievement to support research in Ghana.

**Honors & Distinctions**
* **LSE Teaching Award, Highly Commended** – Recognition for excellence in undergraduate teaching, 2026.
* **Schwarzman College, Outstanding Capstone Award** – Recognition for my master's thesis at Tsinghua University.
* **Phi Beta Kappa** – Inducted into America's oldest academic honor society.
* **University Honors** – Graduated with distinction from Johns Hopkins University.

---
