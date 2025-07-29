## Welcome  

I am a Statistics PhD student at the London School of Economics, interested in using Bayesian methods, machine learning, and computational tools to solve complex problems in risk assessment, toxicology, and healthcare analytics. My advisors are Dr. Sara Geneletti and Dr. Francesca Panero. My research focuses on developing robust statistical models to improve decision-making in health, pharmacology/biotech, toxicology, and risk.

- **Research Interests**: Bayesian inference, dose-response modeling, model averaging, Gaussian processes, probabilistic risk assessment, survival analysis
- **Technical Skills**: R, Python, and SQL, with experience in Bayesian modeling (PyMC3, Stan) and machine learning (TensorFlow, PyTorch)
- **Methodological Focus**: Uncertainty quantification, robust statistical inference, experimental design optimization, model selection and averaging
- **Applications**: 
  - **Academic Research**: Advancing Bayesian model averaging theory, developing robust methods for small-sample inference, creating open-source tools for reproducible risk assessment
  - **Investment Decision Support**: Quantitative due diligence for biotech assets, probability of technical success (PoTS) modeling, risk-adjusted NPV analysis for drug development pipelines, portfolio optimization under uncertainty
  - **Regulatory Science & Strategy**: Benchmark dose estimation for FDA/EMA submissions, prior sensitivity analysis for regulatory compliance, optimal study design to maximize approval probability while minimizing cost
  - **Drug Development Optimization**: Adaptive trial design, go/no-go decision frameworks, cross-regional data harmonization (US/EU/Asia), in-silico patient population generation for trial planning
  - **Healthcare Data Science**: Causal inference from real-world evidence, synthetic control methods for post-market surveillance, generative models for rare disease data augmentation

---

## Current Projects
  - **Bayesian Ensemble Methods for Robust Dose-Response Modeling**: This project develops a novel Dirichlet-weighted stacking approach to combine multiple dose-response models, addressing the critical issue of model uncertainty in risk assessment. Unlike traditional Bayesian Model Averaging, this method uses predictive performance to weight models and places a Dirichlet prior on the weights themselves, creating a distribution rather than point estimates. Expected outcomes include more honest uncertainty quantification and robust risk estimates that don't collapse to single-model solutions, providing better decision support for regulatory submissions and investment due diligence.

- **Adaptive Ensemble Methods for Energy Markets Derivative Trading**: This project explores a framework for trading price spreads in electricity markets, specifically focusing on day-ahead and real-time (DART) spreads. Working with industry practitioners, the research addresses the dual challenge of maximizing predictive accuracy while managing tail risks in volatile energy markets. The framework incorporates multiple risk management layers including model certainty thresholds, tail risk quantification via quantile regression, training distance metrics to avoid extrapolation errors, and dynamic volume adjustment based on regime identification. Expected outcomes include a robust trading system that adapts to changing market conditions while maintaining strict risk controls, and methodological contributions to uncertainty quantification in high-stakes prediction tasks.

- **Generative Models for Context-Conditioned Tabular Data Translation**: This project explores unpaired domain translation for heterogeneous tabular data using both Generative Adversarial Networks (GANs) and Diffusion models. Motivated by the need to harmonize clinical trial data across regions (e.g., US vs. EU), the research develops two frameworks: a Conditional CycleGAN with learned embeddings and explicit conditioning, and a Mixed-Type Cycle-Consistent Diffusion model handling both numerical and categorical features. Using a custom-generated dataset of 40,000 synthetic schizophrenia trial records with systematic US-EU differences, the study addresses challenges of mixed data types, one-to-many mappings, and cycle consistency in tabular contexts. The Conditional CycleGAN achieved structural consistency (cycle reconstruction MSE < 0.01) and reasonable global distribution matching (MMD = 0.001), though with imperfect feature-level fidelity. The Diffusion model, while theoretically promising, failed to learn the translation task effectively. Expected outcomes include validated frameworks for tabular domain translation, insights into the limitations of image-based techniques for heterogeneous data, and recommendations for tabular-specific consistency metrics and evaluation protocols.

- **Comparative Analysis of Likelihoods for Overdispersed Dose-Response Data**: This research systematically evaluates binomial versus beta-binomial likelihoods for Bayesian dose-response modeling in the presence of biological overdispersion. Traditional binomial models assume constant response probability within dose groups, potentially leading to false precision when this assumption is violated. The study implements nine standard dose-response models with both likelihood formulations, using a beta-binomial parameterization that includes a precision parameter $\phi$ to capture extra-binomial variance. Through simulation of 30 datasets with known overdispersion ($\phi=10$), the analysis demonstrates that beta-binomial models provide superior BMD estimation and more realistic uncertainty quantification. 

- **Prior Sensitivity Analysis in Regulatory Benchmark Dose Estimation**: This research investigates how EPA default priors impact Benchmark Dose (BMD) estimates compared to weakly informative alternatives. Using both simulated data and real antimony toxicology data from the National Toxicology Program, the project reveals that restrictive default priors can cause up to 31-fold differences in BMD estimates when prior-data conflicts exist. Expected outcomes include evidence-based recommendations for prior selection in regulatory submissions and a framework for conducting prior sensitivity analyses as standard practice.

- **Optimal Dose Allocation Strategies Under Biological Overdispersion**: This project systematically evaluates experimental design strategies for dose-response studies under realistic conditions of biological variability. It compares different dose-spacing strategies to quantify trade-offs between total sample size, number of dose groups, and allocation strategy. Expected outcomes include practical guidelines for designing more cost-efficient preclinical studies that maximize information gain per dollar spent.

- **Data Integrity in Dose-Response Analysis: The Cost of Dropping Doses**: This research quantifies the statistical damage caused by excluding "inconvenient" dose groups from analysis—a practice sometimes used to achieve cleaner model fits. Through systematic simulation across multiple noise structures, the project demonstrates that dropping even a single dose group can double the uncertainty in BMD estimates. Expected outcomes include evidence-based policies against data exclusion and improved standards for analytical transparency in both internal R&D and regulatory submissions.

- **Non-Parametric Dose-Response Simulation Using Conditional GANs**: This project pushes the boundaries of synthetic data generation by implementing conditional Generative Adversarial Networks (cGANs) for toxicology applications. Moving beyond parametric assumptions, the framework learns complex dose-response relationships directly from data. Three generator architectures are compared, with the most advanced variant learning its own latent noise distribution. Expected outcomes include the ability to create "digital twin" datasets for model validation and data augmentation in scenarios with limited real-world samples.

---

## Education  
- **PhD, Statistics**: London School of Economics (Present)  
- **MSc, Statistics (Research)**: London School of Economics  
- **MMSc, Global Affairs, Economics and Business**: Tsinghua University, Schwarzman College  
- **BA, Public Health**: Johns Hopkins University  

---

## Skills  
- **Statistical Methods**: Bayesian inference, MCMC, optimization, survival analysis, random effects models
- **Programming Languages**: R, Python, SQL

#### Tools
- **Bayesian Modeling**: PyMC3, Stan
- **Machine Learning**: TensorFlow, PyTorch, Scikit-learn  
- **Optimization**: Gurobi, CPLEX, PuLP  

---

## Past Projects  
Some of my past projects have included the following:  

- **Global Financial Tuberculosis Management**: This project examined the financial outlays associated with public health interventions for tuberculosis (TB) using data from the World Health Organization (WHO). We applied regression models for predicting cost overages in TB programs and utilized classification approaches to validate regional strategies. We identified abnormalities in country-level resource allocation for TB programs, and our classification analysis suggest that regional management techniques should be reconsidered. 

- **Antimony Toxicology Risk Assessment**: Completed the first Bayesian dose-response assessment of antimony trioxide, analyzing data from a two-year NTP inhalation study on female mice. Applied three complementary Bayesian methods—parametric modeling, model averaging, and Gaussian process regression—to characterize the relationship between antimony exposure and alveolar/bronchiolar cancer incidence. Results revealed a steep increase in cancer risk at low doses (0.00-0.63 mg/kg-bw/day) followed by a plateau, suggesting non-linear dose-response dynamics with important implications for occupational exposure limits and regulatory standards.

- **Bayesian Regression for Benchmark Dose Estimation**: Implemented nine biologically-plausible parametric models (including Logistic, Probit, Weibull, and Dichotomous Hill) for dose-response assessment using semi-informative priors based on EPA guidance. Applied Bayesian inference via Stan/MCMC to estimate risk functions and benchmark doses, with model selection based on BIC criteria. For antimony data, the Log-Probit model demonstrated superior fit, though only three of nine models adequately captured the non-monotonic response pattern, highlighting the importance of model selection in regulatory risk assessment.

- **Bayesian Model Averaging**: Developed a novel BMA framework for dose-response modeling that weights nine parametric models by their posterior probabilities, calculated via bridge sampling for computational efficiency. This approach addresses model uncertainty—a critical limitation in traditional single-model selection—by incorporating all plausible models weighted by their evidence. For antimony assessment, the Log-Logistic and Log-Probit models dominated with >99% combined weight, producing robust risk estimates with reduced uncertainty in regions of model consensus.

- **Gaussian Process Regression**: Implemented a non-parametric GPR approach using radial basis function kernels with monotonicity and bound constraints to ensure biologically-plausible dose-response curves. The method required only minimal assumptions while flexibly capturing complex relationships in toxicology data. Optimized hyperparameters via marginal likelihood maximization, achieving excellent fit with lower computational demands than model averaging approaches. Results validated the shape of parametric estimates while providing an assumption-free benchmark for model comparison.

- **Exploring Mental Health Predictors in EU Countries**: This report investigated the factors that predict mental health in the European Union (EU). We found that education level, social exclusion, gender tension, self-reported para-emotional assessments, and country effects across EU states were particularly impactful. Our findings indicated that while including hierarchical structures for country-level variation is logical, it does not significantly reduce unexplained variance in the models. Furthermore, factors such as gender tension and self-reported para-emotional assessments were more predictive of mental wellbeing than more complex analyses.

- **Dynamic Adjustment of Healthcare Resources to Reduce Asthma-related ER Visits in California**: This research attempted to predict asthma-related ER visits in California, emphasizing the roles of PM2.5 concentrations and demographics. Despite exploring various models, such as spatial and spatial-temporal approaches, the most insightful was an ecological regression model that included spatial components. The study revealed consistent trends but indicated the need for a broader range of predictors and more granular temporal data.

- **Demographic Differences in Benzodiazepine Use**: This study explored gender differences in benzodiazepine use in relation to personality traits, behaviors, and other substance use. Using ordinal logistic regression, we found that neuroticism was positively associated with benzodiazepine use for both genders, while higher conscientiousness, especially among women, was linked to lower use levels. Interestingly, cannabis, but not alcohol, was associated with increased benzodiazepine use, indicating polysubstance use behavior. The analysis highlighted gender differences in how personality traits and behaviors influence benzodiazepine consumption patterns. 

---

## Papers  
Here are some of my academic contributions:  

- **Bayesian Dose-Response Modeling for Toxicology Risk Assessment with Application to Antimony Trioxide**  
  Wrobleski, T.L. *Master’s Dissertation, London School of Economics and Political Science*, 2024.  

- **Measuring Hospital Contributions to Community Health**  
  Plott, C., Wrobleski, T.L., Sharfstein, J.M., and Thornton, R.L.J. *Johns Hopkins Center for Health Equity. Bloomberg American Health Initiative*, 2021.  

- **The Urgency and Challenge of Opening K-12 Schools in the Fall of 2020**  
  Sharfstein, J.M. and Morphew, C.C. (Wrobleski, T.L. – research assistance). *JAMA*, 324(2):133-134, 2020.  

- **Enhancing Community Engagement by Schools and Programs of Public Health in the United States**  
  Levin, M.B., Bowie, J.V., Ragsdale, S.K., Gawad, A.L., Cooper, L.A., and Sharfstein, J.M. (Brahmbhatt, H., and Wrobleski, T.L. – research assistance). *Annual Review of Public Health*, 42(1):405–21, 2020.  

- **Kidney Donation in China: How Exchange Mechanisms Can Meet Increasing Demand (中国的肾脏捐赠: 肾脏交换机制如何满足增长的肾源需求)**  
  Wrobleski, T.L. *Master’s Capstone, Schwarzman College, Tsinghua University*, 2019.  

- **Preventing Road Traffic Injuries in Jamaica: Gap Analysis and Recommendations**  
  Gielen, A.C., Pollack Porter, K., Wrobleski, T.L., and Tsai, S.H.L. *The Johns Hopkins Center for Injury Research and Policy*, 2018. Prepared for The National Road Safety Council of Jamaica.  

- **Review on Methods of National Goal Setting for the Reduction of Non-Communicable Diseases in Low and Middle-Income Countries**  
  Wrobleski, T.L. and Bukhman, G. *Partners In Health – NCD Synergies*, 2015.  

---

## Awards and Recognition

- **Economic and Social Research Council (ESRC) Doctoral Training Program Studentship**: Awarded competitive funding to support PhD research in statistics at the London School of Economics.  
- **Schwarzman College, Outstanding Capstone Award**: Recognized for excellence in master's thesis at Tsinghua University.  
- **Bloomberg Fellow**: Selected as a fellow in this prestigious program for leadership potential and academic excellence in global affairs.  
- **Phi Beta Kappa**: Inducted into the nation's oldest and most prestigious academic honor society, recognizing exceptional academic achievement.  
- **University Honors**: Graduated with distinction from Johns Hopkins University, acknowledging outstanding academic performance and commitment to excellence.  
- **Gilman Scholarship**: Awarded for academic achievement and commitment to international education, supporting studies and research in Ghana.  

---

## Personal Projects  
I also enjoy building some personal projects to explore ideas and technologies. Here are a few current examples:  

- **ToxDB: Open-Source Platform for Standardized Toxicology Data Collection**: This project develops a web application to address the fragmentation of toxicology data across disparate formats and systems. Built with Flask and SQLAlchemy, ToxDB implements a hierarchical data model (Study → Animal Model → Dose Group → Outcome). The platform features controlled vocabularies for standardizing sex, dose units, exposure routes, and outcome types, while maintaining flexibility through a dynamic metadata system that allows custom fields at any hierarchical level. The workflow reduces data entry errors and ensures completeness, particularly important for complex multi-dose, multi-outcome studies. Expected outcomes include facilitating cross-study comparisons for regulatory submissions, enabling robust meta-analyses for benchmark dose estimation, supporting reproducible risk assessments through standardized data structures, and creating a comprehensive repository for training next-generation dose-response models. The project directly supports my research in Bayesian dose-response modeling by providing high-quality, structured data for model validation and prior elicitation. [GitHub ToxBase](https://github.com/TrevorWrobleski/ToxBase)
- **Real-Time Wildlife Monitoring System**: Multi-stage computer vision project for backyard wildlife management using deep learning and edge computing. The system employs a hierarchical object detection pipeline to first identify general animal categories (birds, squirrels, raccoons) in real-time video streams, then performs fine-grained bird species classification with visit logging to a SQL database. Currently implementing TensorFlow-based models (MobileNetV2, EfficientDet) optimized for edge deployment, with plans to integrate an intelligent deterrent system using reinforcement learning to selectively discourage squirrels and raccoons while preserving bird feeding areas.
- **Battleship-Inspired Search Optimization**: Predictive modeling and search algorithm project that leverages prior knowledge from multiple “experts” (e.g., past history, demographics, and strategy) to optimize the search for a hidden target. Built with Python, this project uses Bayesian inference to combine expert input into a dynamic probability map and implements search algorithms - such as Greedy Search, Monte Carlo Tree Search (MCTS), Reinforcement Learning, and Information Gain - to balance exploration of new areas and exploitation of high-probability regions.
- **Translation & Transcription Tool**: An on-device, live application that transcribes and translates text between English and Chinese (considering context) to support human interpreters. 
- **Thoroughbred Pricing**: Predictive model to estimate the value of thoroughbred racehorses based on factors such as pedigree, physical attributes, racing performance, and market trends. Exploring drivers of racehorses as assets to consider the earning potential and costs of the horses across life stages.
- **Traumatic Brain Injury Rehabilitation**: Predictive model to assess recovery trajectories for patients with traumatic brain injuries (TBI). By integrating patient-specific variables, treatment protocols, and therapy progress data, we seek to support decision-making processes for healthcare providers in occupational and physical therapy settings. Still exploring methods such as Random Forests, Gradient Boosting Machines, and Recurrent Neural Networks to model interactions and time-series nature of the data. 


---

## About Me  
Outside of research, I enjoy running, tennis, hiking, reading, and playing piano. 

You can contact me from my [university page](https://www.lse.ac.uk/statistics/people/trevor-wrobleski).

---

