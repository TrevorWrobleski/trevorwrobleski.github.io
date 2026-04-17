[Home](index.md) | [Research](research.md) | [Projects & Awards](projects.md)

---

## Current Research

**Variance Propagation in Poly-k Survival-Adjusted BMD Estimation**: This ongoing research addresses a methodological gap in carcinogenicity bioassays: treating Poly-k survival-adjusted tumor rates as fixed constants. Current regulatory practice ignores the sampling variability and correlation induced by the adjustment itself. The project develops a variance-aware Bayesian framework that propagates variance directly into the likelihood using group-specific variance inflation factors. Preliminary results indicate that properly accounting for this uncertainty mitigates artificial curve steepness and stabilizes the Benchmark Dose estimate in high-mortality studies.

**Bayesian Ensemble Methods for Robust Dose-Response Modeling**: This project develops a novel Dirichlet-weighted stacking approach to combine multiple dose-response models, addressing the critical issue of model uncertainty in risk assessment. Unlike traditional Bayesian Model Averaging, this method uses predictive performance to weight models and places a Dirichlet prior on the weights themselves, creating a distribution rather than point estimates. Expected outcomes include more honest uncertainty quantification and robust risk estimates that don't collapse to single-model solutions, providing better decision support for regulatory submissions and investment due diligence.

**Adaptive Ensemble Methods for Energy Markets Derivative Trading**: This project explores a framework for trading price spreads in electricity markets, specifically focusing on day-ahead and real-time (DART) spreads. Working with industry practitioners, the research addresses the dual challenge of maximizing predictive accuracy while managing tail risks in volatile energy markets. The framework incorporates multiple risk management layers including model certainty thresholds, tail risk quantification via quantile regression, training distance metrics to avoid extrapolation errors, and dynamic volume adjustment based on regime identification. Expected outcomes include a robust trading system that adapts to changing market conditions while maintaining strict risk controls, and methodological contributions to uncertainty quantification in high-stakes prediction tasks.

---

## Presentations & Conference Talks

### 2026

**Propagating Survival-Adjustment Uncertainty into Risk Analysis**
*Department of Statistics, London School of Economics, London, UK*  
May 2026

<details>
<summary>View Abstract</summary>

Current benchmark dose (BMD) software treats the survival-adjusted denominators as fixed constants, ignoring the additional sampling variability. We develop a beta-binomial likelihood with group-specific overdispersion calibrated to the Bieler-Williams variance inflation, preserving standard BMD estimands while propagating survival-adjustment uncertainty. We extend this to a Bayesian framework with anchored priors on overdispersion and hierarchical pooling of dose-response shape across endpoints. Simulations show that naive binomial models maintain adequate coverage in many settings but exhibit positive bias under severe differential mortality. The variance-aware methods correct this bias and provide honest uncertainty quantification, while hierarchical pooling stabilizes inference for sparse endpoints.

</details>

---

**Empirical Priors for Benchmark Dose Estimation from a Hierarchical Analysis of the Carcinogenic Potency Database**  
*Research Showcase, London School of Economics, London, UK*  
May 2026

<details>
<summary>View Abstract</summary>

In Bayesian dose-response modeling, priors placed on native model parameters (scale and shape coefficients) induce an implicit prior on the benchmark dose (BMD) — a nonlinear functional of those parameters — that can penalize high-curvature dose-response shapes or leave the BMD poorly identified in sparse datasets. We propose a two-part solution: reparameterize dose-response models so the BMD enters as a primary parameter, decoupling potency from curvature in the prior structure, and derive an empirical prior for the BMD through a hierarchical analysis of the Carcinogenic Potency Database. After constructing a validated harmonization rule to incorporate NCI/NTP bioassay records alongside published literature, we analyze 4,754 experiments on 588 chemicals. A hierarchical logistic mixed-effects model decomposes heterogeneity into chemical-level, study-level, and chemical-specific slope variance components, establishing that between-chemical variation in dose-response steepness exceeds the population-average slope. A hierarchical Weibull model, reparameterized with BMD₁₀ as a latent chemical-level parameter under a shared population-level shape, yields the empirical prior ln(BMD₁₀ [g/kg]) ~ N(−4.20, 3.67²). Sensitivity analyses under Hill, logistic, and multistage-2 formulations show that the location and scale of the elicited distribution are stable across models with explicit curvature parameters but inflate under models that lack one. A series of case studies with three-way prior-sensitivity comparisons disentangle the contributions of reparameterization and prior information: in data-rich nonlinear settings, the reparameterization alone preserves the data-supported curve shape regardless of the BMD prior chosen, while in sparse settings the empirical prior provides the regularization that diffuse alternatives cannot. We discuss the computational compromises required at this scale — fixed background rates, a shared shape parameter, exclusion of confounded covariates — and their implications for the interpretation and application of the resulting prior.

</details>

---

**Covariate-Dependent Forecast Combination via Stacked Gibbs Posterior Optimization**  
*Schwarzman College, Tsinghua University, Beijing, China*  
April 2026

<details>
<summary>View Abstract</summary>

Combining probabilistic forecasts from multiple sources into a single ensemble presents a set of challenges: equal weighting ignores differences in model skill, Bayesian model averaging tends to concentrate mass on a single forecaster, and point-optimized weights provide no uncertainty quantification. We introduce the Covariate-Dependent Stacked Gibbs Posterior (CD-SGP), which replaces the global weight vector with covariate-dependent weights parameterized by a softmax gating network, allowing ensemble composition to adapt to observable context while inheriting the SGP's scoring-rule optimization and uncertainty quantification. In a regime-switching simulation, the CD-SGP improves upon the SGP by 15.6% in mean CRPS. On the FluSight data with normalized time as a single covariate, the CD-SGP achieves the best performance among all methods compared, learning interpretable weight dynamics that reveal how forecaster skill evolves over the flu season. The method's built-in shrinkage toward global weights ensures it cannot perform substantially worse than its static counterpart, making it a practical default for settings where the relative quality of competing forecasts may vary with context.

</details>

---

**Efficient Bayesian Experimental Design for Benchmark Dose Estimation Under Overdispersion**  
*Cumberland Lodge Retreat, Windsor, UK*  
January 2026

<details>
<summary>View Abstract</summary>

Benchmark dose (BMD) estimation is foundational to regulatory toxicology, yet standard experimental designs rarely account for the overdispersion that pervades real bioassay data. This talk presents results from a large-scale Bayesian simulation study that evaluates how three resource-allocation levers — dose placement strategy, total sample size (N), and number of dose groups (G) — jointly determine BMD estimation accuracy and precision under a Beta-Binomial data-generating process (φ = 10, ICC ≈ 0.09). Across 2,700 simulated experiments spanning six placement strategies, five group counts, and three sample sizes, we find that dose placement is the dominant driver of estimation accuracy: a D-Optimal design with N = 240 achieves roughly five-fold lower mean squared error than a conventional equally-spaced design with twice as many subjects. Increasing the number of dose groups yields substantial gains under efficient placement but marginal improvement under suboptimal designs, while increasing sample size alone offers diminishing returns without a sound allocation strategy. These findings reframe the traditional explore-versus-replicate trade-off and point toward design-first principles for more ethical and cost-efficient toxicology experiments. The talk concludes by situating these results within a broader inference pipeline, highlighting the complementary roles of likelihood specification, dose-group handling, and prior sensitivity in achieving robust BMD estimates.

</details>

---

### 2025

**Robustness and Sensitivity in Bayesian Dose-Response Risk Assessment**  
*Sapienza University of Rome, Rome, Italy*  
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

**Generative Models for Context-Conditioned Tabular Data Translation**: This project explores unpaired domain translation for heterogeneous tabular data using both Generative Adversarial Networks (GANs) and Diffusion models.
* **Methodology:** Motivated by the need to harmonize clinical trial data (e.g., US vs. EU), developed a Conditional CycleGAN with learned embeddings and explicit conditioning, and a Mixed-Type Cycle-Consistent Diffusion model.
* **Result:** The CycleGAN achieved structural consistency (cycle reconstruction MSE < 0.01) and global distribution matching (MMD = 0.001). The Diffusion model, while theoretically promising, failed to learn the translation task effectively.
* **Outcomes:** Validated frameworks for tabular domain translation, insights into limitations of image-based techniques for heterogeneous data, and recommendations for tabular-specific consistency metrics. [GitHub Repository](https://github.com/TrevorWrobleski/tabular-domain-translation)

**Comparative Analysis of Likelihoods for Overdispersed Dose-Response Data**: This research evaluated the inferential impact of likelihood misspecification in the presence of biological overdispersion ($\phi=10$). The study compared Binomial versus Beta-Binomial formulations across nine standard dose-response models using Bayesian inference.
* **Key Finding:** Misspecified Binomial models exhibited "false precision," producing artificially narrow credible intervals that failed to capture true risk levels. The switch to a Beta-Binomial parameterization induced massive distributional shifts (Symmetrized KL divergence $D_{\mathrm{SKL}} > 2.8$ across all models), correcting the underestimation of variance. 
* **Outcome:** Validated the Beta-Binomial likelihood as essential for honest uncertainty quantification in toxicology, preventing the false confidence associated with standard regulatory models.

**Prior Sensitivity Analysis in Regulatory Benchmark Dose Estimation**: This project quantified the inferential leverage of EPA default priors versus weakly informative alternatives using Morris elementary-effect screening and local sensitivity sweeps. The analysis utilized both simulated datasets and experimental antimony trioxide bioassay data.
* **Key Finding:** The prior on the Hill coefficient (k) was identified as the dominant driver of estimation variance. In the antimony case study, adhering to restrictive EPA defaults versus data-driven priors resulted in a **31-fold difference** in the final Benchmark Dose estimate ($0.031$ vs $0.001$).
* **Outcome:** Demonstrated that default priors can silently override experimental data in sparse bioassays, supporting a move toward routine prior sensitivity diagnostics in regulatory submissions.

**Optimizing Resource Allocation in Toxicology Experiments with Overdispersed Quantal Data**: This study systematically evaluated the efficiency of six experimental design strategies (including D-Optimal, c-Optimal, and heuristic approaches) under conditions of biological overdispersion ($\phi=10$). Using a large-scale Bayesian simulation framework, the research quantified the variance-bias trade-offs between total sample size ($N$), number of dose groups ($G$), and dose placement.
* **Key Finding:** Allocation strategy is the dominant driver of estimation accuracy. A D-Optimal design with $N=240$ subjects achieved a **five-fold reduction in Mean Squared Error (MSE)** compared to a traditional equally-spaced design with $N=480$ subjects.
* **Outcome:** The results demonstrate that maximizing the number of dose groups ($G \ge 8$) within a D-Optimal framework yields higher information gain than simply increasing sample size, providing a blueprint for more ethical and cost-efficient bioassays.

**Data Integrity in Dose-Response Analysis: The Cost of Dropping Doses**: This study quantified the statistical information loss and variance inflation caused by excluding dose groups in Bayesian benchmark dose (BMD) estimation. Using the Dichotomous Hill model, the research employed simulations across Binomial, Uniform, and Beta-Binomial noise structures, alongside an experimental case study of antimony trioxide.
* **Key Finding:** Selective deletion of the mid-range dose—the region most informative for the Hill coefficient (k)—doubled the width of the 95% credible interval and induced large distributional shifts (Symmetrized KL divergence $D_{\mathrm{SKL}} \approx 0.8$).
* **Outcome:** The analysis demonstrated that dose deletion is not merely a precision issue but a distributional distortion, establishing a quantitative basis for enforcing data inclusion in regulatory submissions.

**Non-Parametric Dose-Response Simulation Using Conditional GANs**: This project developed a methodological framework for generating synthetic toxicology data using Conditional Generative Adversarial Networks (cGANs), addressing the limitations of standard parametric assumptions.
* **Methodology:** The study implemented and compared three generator architectures to learn complex dose-response relationships directly from tabular bioassay data. The optimal architecture incorporated a learned latent noise distribution to capture biological stochasticity. 
* **Result:** The framework generated "digital twin" datasets that preserved the statistical properties of the original samples, validating the use of cGANs for data augmentation in sparse toxicological scenarios.

**Global Financial Tuberculosis Management**: This project examined the financial outlays associated with public health interventions for tuberculosis (TB) using data from the World Health Organization (WHO).
* **Methodology:** Applied regression models for predicting cost overages in TB programs and utilized classification approaches to validate regional strategies.
* **Key Finding:** Identified abnormalities in country-level resource allocation for TB programs; classification analysis suggests that regional management techniques should be reconsidered.

**Antimony Toxicology Risk Assessment**: Completed the first Bayesian dose-response assessment of antimony trioxide, analyzing data from a two-year NTP inhalation study on female mice.
* **Methodology:** Applied three complementary Bayesian methods—parametric modeling, model averaging, and Gaussian process regression—to characterize the relationship between antimony exposure and alveolar/bronchiolar cancer incidence.
* **Key Finding:** Results revealed a steep increase in cancer risk at low doses (0.00-0.63 mg/kg-bw/day) followed by a plateau, suggesting non-linear dose-response dynamics with important implications for occupational exposure limits and regulatory standards.

**Bayesian Regression for Benchmark Dose Estimation**: Implemented nine biologically-plausible parametric models (including Logistic, Probit, Weibull, and Dichotomous Hill) for dose-response assessment using semi-informative priors based on EPA guidance.
* **Methodology:** Applied Bayesian inference via Stan/MCMC to estimate risk functions and benchmark doses, with model selection based on BIC criteria.
* **Key Finding:** For antimony data, the Log-Probit model demonstrated superior fit, though only three of nine models adequately captured the non-monotonic response pattern, highlighting the importance of model selection in regulatory risk assessment.

**Bayesian Model Averaging**: Developed a novel BMA framework for dose-response modeling that weights nine parametric models by their posterior probabilities, calculated via bridge sampling for computational efficiency.
* **Focus:** Addresses model uncertainty by incorporating plausible EPA models weighted by their evidence.
* **Result:** For antimony assessment, the Log-Logistic and Log-Probit models dominated with >99% combined weight, producing robust risk estimates with reduced uncertainty in regions of model consensus.

**Gaussian Process Regression**: Implemented a non-parametric GPR approach using radial basis function kernels with monotonicity and bound constraints to ensure biologically-plausible dose-response curves.
* **Methodology:** Optimized hyperparameters via marginal likelihood maximization, achieving excellent fit with lower computational demands than model averaging approaches.
* **Outcome:** Validated the shape of parametric estimates while providing an assumption-free benchmark for model comparison, requiring minimal assumptions to capture complex relationships in toxicology data.

**Exploring Mental Health Predictors in EU Countries**: This report investigated the factors that predict mental health in the European Union (EU).
* **Key Finding:** Education level, social exclusion, gender tension, self-reported para-emotional assessments, and country effects across EU states were particularly impactful.
* **Result:** Hierarchical structures for country-level variation were logical but did not significantly reduce unexplained variance; factors such as gender tension and self-reported para-emotional assessments were more predictive of mental wellbeing than more complex analyses.

**Dynamic Adjustment of Healthcare Resources to Reduce Asthma-related ER Visits in California**: This research attempted to predict asthma-related ER visits in California, emphasizing the roles of PM2.5 concentrations and demographics.
* **Methodology:** Explored various models, such as spatial and spatial-temporal approaches; the most insightful was an ecological regression model that included spatial components.
* **Outcome:** Revealed consistent trends but indicated the need for a broader range of predictors and more granular temporal data.

**Demographic Differences in Benzodiazepine Use**: This study explored gender differences in benzodiazepine use in relation to personality traits, behaviors, and other substance use.
* **Methodology:** Using ordinal logistic regression, found that neuroticism was positively associated with benzodiazepine use for both genders.
* **Key Finding:** Higher conscientiousness, especially among women, was linked to lower use levels. Interestingly, cannabis, but not alcohol, was associated with increased benzodiazepine use, indicating polysubstance use behavior.

---
