# Place Matters: Regional Risks in Breast Cancer Mortality

*The Influence of Clinical and Structural Factors on In-Hospital Breast Cancer Mortality Among Black Women*

## Executive Summary

**Problem:** Black women in the United States experience disproportionately high breast cancer mortality, yet the specific drivers of in-hospital death, particularly the role of structural inequities beyond clinical severity, remain underexamined.

## Methodology

This study analyzes **5,934 hospitalizations** from the 2021 National Inpatient Sample with machine learning.

- **Data Preparation:** Extraction of breast cancer hospitalizations using ICD-10 code C50. Cleaning and recoding of clinical and structural variables. Application of discharge weights to produce nationally representative estimates. Handling of categorical variables through encoding and normalization.
- **Exploratory Data Analysis:** Descriptive statistics of demographic, clinical, and structural variables. Comparative analysis across geographic regions and socioeconomic strata.
- **Statistical & Machine Learning Models:** Six predictive models were trained and compared:
    - Logistic Regression (L1/L2) Baseline statistical model used for both inference and prediction. Achieved the highest cross-validated performance (CV AUC ≈ 0.71), indicating that relationships between predictors and mortality are largely linear and additive.
    - Elastic Net Combines L1 and L2 regularization for feature selection and multicollinearity handling. Demonstrated reduced predictive performance (CV AUC ≈ 0.62), suggesting important predictors were over-shrunk.
    - Random Forest Ensemble tree-based model capable of capturing nonlinear relationships and interactions (CV AUC ≈ 0.66).
    - Gradient Boosting (GBM) Sequential ensemble method designed to improve predictive accuracy. Best-performing nonlinear model, but still below logistic regression (CV AUC ≈ 0.68).
    - XGBoost Optimized gradient boosting algorithm tailored for imbalanced data. Performance comparable to GBM but did not outperform the linear model (CV AUC ≈ 0.67).
  
  Training/Validation Split: 70% / 30% | Evaluation Metric: Area Under the ROC Curve (AUC)<br>
  Feature Importance: Assessed using permutation importance.

### Key Features

- Race-Specific Analysis: Focus exclusively on non-Hispanic Black women.
- Nationally Representative Estimates: Use of NIS discharge weights.
- Integration of Clinical and Structural Determinants.
- Machine Learning–Driven Risk Prediction.
- Structural Inequity Gap: Quantifies mortality differences attributable to systemic factors.
- Regional Analysis: Highlights disparities across U.S. Census divisions.

## Key Findings

- **In-Hospital Mortality Rate:** **5.3%** among Black women.
- **Strongest Clinical Predictor:** Metastatic disease (**OR ≈ 2.18**).
- **Key Structural Predictors:**
  - Geographic Region: Highest risk in the **South (Division 6)** and lowest in Division 8.
  - Insurance Status: Self-pay and Medicaid associated with higher mortality.
  - Socioeconomic Status: Lower ZIP income quartiles linked to increased risk.
  - Admission Type: Non-elective admissions significantly increase mortality.
- **Structural Inequity Gap:** Up to a **37‑percentage‑point difference** in predicted mortality between high‑ and low‑risk regions. A model‑based dashboard was created for user exploration of the inequity gap.

---

## Breast Cancer Mortality in Black Women – Datastory

<div class="flourish-embed flourish-chart" data-src="story/3646484">
    <script src="https://public.flourish.studio/resources/embed.js"></script>
    <noscript>
        <img src="https://public.flourish.studio/story/3646484/thumbnail" width="100%" alt="visualization" />
    </noscript>
</div>

## Breast Cancer Mortality in Black Women – Interactive Model Based Dashboard

<div class='tableauPlaceholder' id='viz1776816804475' style='position: relative'>
    <noscript>
        <a href='#'>
            <img alt='Breast Cancer Mortality Risk Predictor- NIS 2021' src='https://public.tableau.com/static/images/Bl/BlackFemaleMortalityModel/Dashboard1/1_rss.png' style='border: none' />
        </a>
    </noscript>
    <object class='tableauViz' style='display:none;'>
        <param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' />
        <param name='embed_code_version' value='3' />
        <param name='site_root' value='' />
        <param name='name' value='BlackFemaleMortalityModel/Dashboard1' />
        <param name='tabs' value='no' />
        <param name='toolbar' value='yes' />
        <param name='static_image' value='https://public.tableau.com/static/images/Bl/BlackFemaleMortalityModel/Dashboard1/1.png' />
        <param name='animate_transition' value='yes' />
        <param name='display_static_image' value='yes' />
        <param name='display_spinner' value='yes' />
        <param name='display_overlay' value='yes' />
        <param name='display_count' value='yes' />
        <param name='language' value='en-US' />
    </object>
</div>
<script type='text/javascript'>
    var divElement = document.getElementById('viz1776816804475');
    var vizElement = divElement.getElementsByTagName('object')[0];
    if (divElement.offsetWidth > 800) {
        vizElement.style.width = '1720px';
        vizElement.style.minHeight = '887px';
        vizElement.style.maxHeight = '987px';
        vizElement.style.height = (divElement.offsetWidth * 0.75) + 'px';
    } else if (divElement.offsetWidth > 500) {
        vizElement.style.width = '1720px';
        vizElement.style.minHeight = '887px';
        vizElement.style.maxHeight = '987px';
        vizElement.style.height = (divElement.offsetWidth * 0.75) + 'px';
    } else {
        vizElement.style.width = '100%';
        vizElement.style.height = '1727px';
    }
    var scriptElement = document.createElement('script');
    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';
    vizElement.parentNode.insertBefore(scriptElement, vizElement);
</script>

>  **User instructions:** Hover over data points to see exact values. Use filters to explore by region, age, or socioeconomic strata.
