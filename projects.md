[Home](index.md) | [Research](research.md) | [Projects & Awards](projects.md)

---

## Machine Learning & AI

### **Real-Time Wildlife Monitoring System**
**Tech Stack:** TensorFlow (MobileNetV2, EfficientDet), Edge Computing, SQL
A multi-stage computer vision pipeline for wildlife management. The system uses hierarchical object detection to identify general categories (birds, squirrels) in real-time video, followed by fine-grained bird species classification.
* **Current State:** Optimized for edge deployment.
* **Future Dev:** Integrating Deep Reinforcement Learning (DRL) for selective deterrent systems.

### **Vincero Monopoly POMDP: Bayesian Simulation Engine**
**Tech Stack:** Python, NumPy, Gymnasium, Stable-Baselines3 (PPO)

A rules-exact Monopoly simulation built on a Partially Observable Markov Decision Process (POMDP) architecture. The core contribution is a **Monte Carlo win probability estimator** that answers: *given the current board — each player's cash, properties, and buildings — what is each player's probability of winning?*

* **Win Probability Estimation:** Specify any board state (cash holdings, property ownership, building counts) for all players via the `ScenarioBuilder`, and the estimator rolls out hundreds of simulated games — sampling hidden deck permutations and latent opponent risk profiles — to produce P(win \| state) for each player. Parameter sweeps reveal how sensitive these probabilities are to changes in cash, position, or development.
* **POMDP Architecture:** Models Monopoly with genuine information asymmetry — hidden deck order and latent opponent aggressiveness (θ ∈ [0,1]) — rather than treating it as a fully observable optimization problem.
* **Key Findings:** First-mover advantage yields ~6 percentage points over the fair baseline of 25%; aggressive play consistently dominates conservative strategies; the game's tipping point — where one player's advantage becomes statistically irreversible — typically occurs around turns 80–120 when developed monopolies outpace GO salary.
* **RL Integration:** A Gymnasium-wrapped environment (246-dim observation, 90 discrete actions) supports PPO training via Stable-Baselines3 against heuristic opponents.

[View on GitHub](https://github.com/TrevorWrobleski/Vincero)

### **Bayesian Search Optimization ("Battleship" Solver)**
**Tech Stack:** Python, MCTS, Reinforcement Learning
A predictive modeling project leveraging "expert" priors to optimize search efficiency for a hidden target.
* **Methodology:** Uses Bayesian inference to combine expert input into a dynamic probability map.
* **Algorithms:** Implements Greedy Search, Monte Carlo Tree Search (MCTS), and Information Gain metrics to balance the exploration-exploitation trade-off.

### **Context-Aware Translation Tool**
**Tech Stack:** Python, OpenAI Whisper, Hugging Face Transformers (Helsinki-NLP Opus-MT), PyTorch, CustomTkinter
An on-device, live application for transcribing and translating text between English and Chinese (Mandarin). Focuses on context retention to support real-time human interpretation.

---

## Applied Statistics & Modeling

### **Thoroughbred Asset Pricing Model**
**Focus:** Financial Modeling, Regression Analysis
Predictive modeling to estimate the value of thoroughbred racehorses as financial assets. This project integrates pedigree, physical attributes, and market trends to model earning potential and cost structures across the animal's life stages.

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
* **Schwarzman College, Outstanding Capstone Award** – Recognition for Master's thesis excellence at Tsinghua University.
* **Phi Beta Kappa** – Inducted into the nation's oldest academic honor society.
* **University Honors** – Graduated with distinction from Johns Hopkins University.

---
