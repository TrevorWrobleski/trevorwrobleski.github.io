[Home](index.md) | [Research](research.md) | [Projects & Awards](projects.md)

---

## Current Research

**Bayesian Ensemble Methods for Robust Dose-Response Modeling**: This project develops a novel Dirichlet-weighted stacking approach to combine multiple dose-response models, addressing the critical issue of model uncertainty in risk assessment. Unlike traditional Bayesian Model Averaging, this method uses predictive performance to weight models and places a Dirichlet prior on the weights themselves, creating a distribution rather than point estimates. Expected outcomes include more honest uncertainty quantification and robust risk estimates that don't collapse to single-model solutions, providing better decision support for regulatory submissions and investment due diligence.

**Adaptive Ensemble Methods for Energy Markets Derivative Trading**: This project explores a framework for trading price spreads in electricity markets, specifically focusing on day-ahead and real-time (DART) spreads. Working with industry practitioners, the research addresses the dual challenge of maximizing predictive accuracy while managing tail risks in volatile energy markets. The framework incorporates multiple risk management layers including model certainty thresholds, tail risk quantification via quantile regression, training distance metrics to avoid extrapolation errors, and dynamic volume adjustment based on regime identification. Expected outcomes include a robust trading system that adapts to changing market conditions while maintaining strict risk controls, and methodological contributions to uncertainty quantification in high-stakes prediction tasks.

**Comparative Analysis of Likelihoods for Overdispersed Dose-Response Data**: This research systematically evaluates binomial versus beta-binomial likelihoods for Bayesian dose-response modeling in the presence of biological overdispersion. Traditional binomial models assume constant response probability within dose groups, potentially leading to false precision when this assumption is violated. The study implements nine standard dose-response models with both likelihood formulations, using a beta-binomial parameterization that includes a precision parameter φ to capture extra-binomial variance. Through simulation of 30 datasets with known overdispersion (φ=10), the analysis demonstrates that beta-binomial models provide superior BMD estimation and more realistic uncertainty quantification.

**Prior Sensitivity Analysis in Regulatory Benchmark Dose Estimation**: This research investigates how EPA default priors impact Benchmark Dose (BMD) estimates compared to weakly informative alternatives. Using both simulated data and real antimony toxicology data from the National Toxicology Program, the project reveals that restrictive default priors can cause up to 31-fold differences in BMD estimates when prior-data conflicts exist. Expected outcomes include evidence-based recommendations for prior selection in regulatory submissions and a framework for conducting prior sensitivity analyses as standard practice.

**Optimal Dose Allocation Strategies Under Biological Overdispersion**: This project systematically evaluates experimental design strategies for dose-response studies under realistic conditions of biological variability. It compares different dose-spacing strategies to quantify trade-offs between total sample size, number of dose groups, and allocation strategy. Expected outcomes include practical guidelines for designing more cost-efficient preclinical studies that maximize information gain per dollar spent.

**Data Integrity in Dose-Response Analysis: The Cost of Dropping Doses**: This research quantifies the statistical damage caused by excluding "inconvenient" dose groups from analysis—a practice sometimes used to achieve cleaner model fits. Through systematic simulation across multiple noise structures, the project demonstrates that dropping even a single dose group can double the uncertainty in BMD estimates. Expected outcomes include evidence-based policies against data exclusion and improved standards for analytical transparency in both internal R&D and regulatory submissions.

**Non-Parametric Dose-Response Simulation Using Conditional GANs**: This project pushes the boundaries of synthetic data generation by implementing conditional Generative Adversarial Networks (cGANs) for toxicology applications. Moving beyond parametric assumptions, the framework learns complex dose-response relationships directly from data. Three generator architectures are compared, with the most advanced variant learning its own latent noise distribution. Expected outcomes include the ability to create "digital twin" datasets for model validation and data augmentation in scenarios with limited real-world samples.

---

## Presentations & Conference Talks

### 2025

**Robustness and Sensitivity in Bayesian Dose-Response Risk Assessment**  
*Sapienza University of Rome, Italy*  
October 21, 2025 | Sala Corsi, Palazzina Presidenza

<details>
<summary>View Abstract</summary>

Bayesian methods are increasingly central to toxicological risk assessment, yet their application to sparse dose-response data presents unique challenges. This presentation examines three drivers of analytical robustness: (i) the choice of likelihood for overdispersed quantal data, (ii) the inferential impact of selective dose-group deletion, and (iii) the sensitivity of results to prior specification. Using simulations and a case study of antimony trioxide carcinogenicity, we quantify the impact of these choices on benchmark dose (BMD) estimates and the posterior distribution, using metrics like Mean Squared Error and symmetrized Kullback-Leibler (KL) divergence. Our findings show that modeling overdispersion with a Beta-Binomial likelihood is important for accurate uncertainty quantification. We also demonstrate that deleting informative mid-range dose groups can degrade precision and shift inference. Finally, for the Dichotomous Hill model, the prior on the Hill coefficient is the dominant lever on the BMD, capable of inducing multi-fold changes in the risk estimate.

</details>

---

**Experimental Design for Benchmark Dose Estimation Under Overdispersed Data Conditions**  
*Bayes Biostatistics 2025, Leiden, Netherlands*  
October 24, 2025 | [Slides](https://www.bayes-pharma.org/bayes-2025/)

<details>
<summary>View Abstract</summary>

Designing efficient animal chronic toxicolgoy bioassays under fixed resources presents a persistent challenge. Investigators must resolve the trade-off between exploring the dose-response curve (using more dose groups, G) and reducing sampling variance (using more subjects, N). This problem is compounded by overdispersion (e.g., litter effects), a common feature of toxicological data that violates simple binomial assumptions. This research uses a large-scale Bayesian simulation study to evaluate BMD estimation performance under a realistic, overdispersed Beta-Binomial data-generating process. We compare the performance of six distinct dose placement strategies (including D-Optimal, c-Optimal, equal, geometric, and heuristic designs) across a range of total sample sizes and numbers of dose groups. Performance is assessed by evaluating the accuracy (Mean Squared Error, MSE) and precision (95% credible interval width and coverage) of the resulting BMD estimates.

The results demonstrate that the choice of dose placement strategy is a dominant driver of estimation accuracy, often having a greater impact than the total sample size. Furthermore, for efficient strategies like D-Optimal, increasing the number of dose groups (G) substantially improves accuracy by better characterizing the curve. Conversely, for suboptimal strategies, adding more groups offers marginal benefit. We conclude that when designing BMD studies in the presence of overdispersion, allocating resources toward an optimal placement strategy and a higher number of dose groups is critical for minimizing estimation error and maximizing precision.
</details>

---

## Publications  

**Bayesian Dose-Response Modeling for Toxicology Risk Assessment with Application to Antimony Trioxide**  
Wrobleski, T.L. *Master's Dissertation, London School of Economics and Political Science*, 2024.  

**Measuring Hospital Contributions to Community Health**  
Plott, C., Wrobleski, T.L., Sharfstein, J.M., and Thornton, R.L.J. *Johns Hopkins Center for Health Equity. Bloomberg American Health Initiative*, 2021.  

**The Urgency and Challenge of Opening K-12 Schools in the Fall of 2020**  
Sharfstein, J.M. and Morphew, C.C. (Wrobleski, T.L. – research assistance). *JAMA*, 324(2):133-134, 2020.  

**Enhancing Community Engagement by Schools and Programs of Public Health in the United States**  
Levin, M.B., Bowie, J.V., Ragsdale, S.K., Gawad, A.L., Cooper, L.A., and Sharfstein, J.M. (Brahmbhatt, H., and Wrobleski, T.L. – research assistance). *Annual Review of Public Health*, 42(1):405–21, 2020.  

**Kidney Donation in China: How Exchange Mechanisms Can Meet Increasing Demand (中国的肾脏捐赠: 肾脏交换机制如何满足增长的肾源需求)**  
Wrobleski, T.L. *Master's Capstone, Schwarzman College, Tsinghua University*, 2019.  

**Preventing Road Traffic Injuries in Jamaica: Gap Analysis and Recommendations**  
Gielen, A.C., Pollack Porter, K., Wrobleski, T.L., and Tsai, S.H.L. *The Johns Hopkins Center for Injury Research and Policy*, 2018. Prepared for The National Road Safety Council of Jamaica.  

**Review on Methods of National Goal Setting for the Reduction of Non-Communicable Diseases in Low and Middle-Income Countries**  
Wrobleski, T.L. and Bukhman, G. *Partners In Health – NCD Synergies*, 2015.  

---

## Past Research  

**Generative Models for Context-Conditioned Tabular Data Translation**: This project explores unpaired domain translation for heterogeneous tabular data using both Generative Adversarial Networks (GANs) and Diffusion models. Motivated by the need to harmonize clinical trial data across regions (e.g., US vs. EU), the research develops two frameworks: a Conditional CycleGAN with learned embeddings and explicit conditioning, and a Mixed-Type Cycle-Consistent Diffusion model handling both numerical and categorical features. Using a custom-generated dataset of 40,000 synthetic schizophrenia trial records with systematic US-EU differences, the study addresses challenges of mixed data types, one-to-many mappings, and cycle consistency in tabular contexts. The Conditional CycleGAN achieved structural consistency (cycle reconstruction MSE < 0.01) and reasonable global distribution matching (MMD = 0.001), though with imperfect feature-level fidelity. The Diffusion model, while theoretically promising, failed to learn the translation task effectively. Expected outcomes include validated frameworks for tabular domain translation, insights into the limitations of image-based techniques for heterogeneous data, and recommendations for tabular-specific consistency metrics and evaluation protocols. [GitHub Repository](https://github.com/TrevorWrobleski/tabular-domain-translation)

**Global Financial Tuberculosis Management**: This project examined the financial outlays associated with public health interventions for tuberculosis (TB) using data from the World Health Organization (WHO). We applied regression models for predicting cost overages in TB programs and utilized classification approaches to validate regional strategies. We identified abnormalities in country-level resource allocation for TB programs, and our classification analysis suggest that regional management techniques should be reconsidered.

**Antimony Toxicology Risk Assessment**: Completed the first Bayesian dose-response assessment of antimony trioxide, analyzing data from a two-year NTP inhalation study on female mice. Applied three complementary Bayesian methods—parametric modeling, model averaging, and Gaussian process regression—to characterize the relationship between antimony exposure and alveolar/bronchiolar cancer incidence. Results revealed a steep increase in cancer risk at low doses (0.00-0.63 mg/kg-bw/day) followed by a plateau, suggesting non-linear dose-response dynamics with important implications for occupational exposure limits and regulatory standards.

**Bayesian Regression for Benchmark Dose Estimation**: Implemented nine biologically-plausible parametric models (including Logistic, Probit, Weibull, and Dichotomous Hill) for dose-response assessment using semi-informative priors based on EPA guidance. Applied Bayesian inference via Stan/MCMC to estimate risk functions and benchmark doses, with model selection based on BIC criteria. For antimony data, the Log-Probit model demonstrated superior fit, though only three of nine models adequately captured the non-monotonic response pattern, highlighting the importance of model selection in regulatory risk assessment.

**Bayesian Model Averaging**: Developed a novel BMA framework for dose-response modeling that weights nine parametric models by their posterior probabilities, calculated via bridge sampling for computational efficiency. This approach addresses model uncertainty—a critical limitation in traditional single-model selection—by incorporating all plausible models weighted by their evidence. For antimony assessment, the Log-Logistic and Log-Probit models dominated with >99% combined weight, producing robust risk estimates with reduced uncertainty in regions of model consensus.

**Gaussian Process Regression**: Implemented a non-parametric GPR approach using radial basis function kernels with monotonicity and bound constraints to ensure biologically-plausible dose-response curves. The method required only minimal assumptions while flexibly capturing complex relationships in toxicology data. Optimized hyperparameters via marginal likelihood maximization, achieving excellent fit with lower computational demands than model averaging approaches. Results validated the shape of parametric estimates while providing an assumption-free benchmark for model comparison.

**Exploring Mental Health Predictors in EU Countries**: This report investigated the factors that predict mental health in the European Union (EU). We found that education level, social exclusion, gender tension, self-reported para-emotional assessments, and country effects across EU states were particularly impactful. Our findings indicated that while including hierarchical structures for country-level variation is logical, it does not significantly reduce unexplained variance in the models. Furthermore, factors such as gender tension and self-reported para-emotional assessments were more predictive of mental wellbeing than more complex analyses.

**Dynamic Adjustment of Healthcare Resources to Reduce Asthma-related ER Visits in California**: This research attempted to predict asthma-related ER visits in California, emphasizing the roles of PM2.5 concentrations and demographics. Despite exploring various models, such as spatial and spatial-temporal approaches, the most insightful was an ecological regression model that included spatial components. The study revealed consistent trends but indicated the need for a broader range of predictors and more granular temporal data.

**Demographic Differences in Benzodiazepine Use**: This study explored gender differences in benzodiazepine use in relation to personality traits, behaviors, and other substance use. Using ordinal logistic regression, we found that neuroticism was positively associated with benzodiazepine use for both genders, while higher conscientiousness, especially among women, was linked to lower use levels. Interestingly, cannabis, but not alcohol, was associated with increased benzodiazepine use, indicating polysubstance use behavior. The analysis highlighted gender differences in how personality traits and behaviors influence benzodiazepine consumption patterns.

---
