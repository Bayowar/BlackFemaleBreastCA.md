<!DOCTYPE html>
<html>
<head>
    <title>Place Matters: Regional Risks in Breast Cancer Mortality | Black Women NIS Study</title>
    <meta charset="UTF-8">
    <style>
        body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; margin: 0; padding: 20px; background: #fafafa; }
        .container { max-width: 1300px; margin: 0 auto; background: white; padding: 20px; border-radius: 12px; box-shadow: 0 2px 8px rgba(0,0,0,0.05); }
        h1 { color: #1a1a1a; border-bottom: 3px solid #d62828; display: inline-block; padding-bottom: 6px; margin-top: 0; }
        h2 { color: #2c3e50; margin-top: 28px; margin-bottom: 12px; border-left: 4px solid #d62828; padding-left: 15px; }
        h3 { color: #34495e; margin: 20px 0 8px 0; }
        .summary { background: #f0f0f0; padding: 16px; border-radius: 8px; margin: 20px 0; }
        .note { font-size: 0.85rem; color: #555; background: #eef; padding: 10px; border-radius: 6px; margin-top: 20px; }
        .key-finding { background: #fef5e7; border-left: 4px solid #e67e22; padding: 12px 18px; margin: 15px 0; border-radius: 6px; }
        .key-feature { background: #e8f8f5; border-left: 4px solid #1abc9c; padding: 12px 18px; margin: 15px 0; border-radius: 6px; }
        hr { margin: 30px 0; border: 0; height: 1px; background: #ddd; }
        .highlight { font-weight: 600; color: #c0392b; }
    </style>
</head>
<body>
<div class="container">

    <h1>Place Matters: Regional Risks in Breast Cancer Mortality</h1>
    <p style="font-size: 1.2rem; color: #2c3e50; margin-top: 0;">The Influence of Clinical and Structural Factors on In-Hospital Breast Cancer Mortality Among Black Women</p>

    <h2>Executive Summary</h2>
    <div class="summary">
        <strong>Problem:</strong> Black women in the United States experience disproportionately high breast cancer mortality, yet the specific drivers of in-hospital death, particularly the role of structural inequities beyond clinical severity, remain underexamined.
    </div>

    <h2>Methodology</h2>
    <p>This study analyzes <strong>5,934 hospitalizations</strong> from the 2021 National Inpatient Sample using a machine learning framework.</p>
    <ul>
        <li><strong>Data Preparation:</strong> Extraction of breast cancer hospitalizations using ICD-10 code C50. Cleaning and recoding of clinical and structural variables. Application of discharge weights to produce nationally representative estimates. Handling of categorical variables through encoding and normalization.</li>
        <li><strong>Exploratory Data Analysis:</strong> Descriptive statistics of demographic, clinical, and structural variables. Comparative analysis across geographic regions and socioeconomic strata.</li>
        <li><strong>Statistical & Machine Learning Models:</strong> Six predictive models were trained and compared:
            <ul>
                <li>Logistic Regression (L1/L2) – Baseline statistical inference</li>
                <li><strong>Elastic Net (Best Model)</strong> – Handles multicollinearity and feature selection (AUC ≈ 0.69)</li>
                <li>Random Forest – Captures nonlinear relationships</li>
                <li>Gradient Boosting (GBM) – Enhances predictive performance</li>
                <li>XGBoost – Optimized ensemble learning</li>
            </ul>
            Training/Validation Split: 70% / 30% | Evaluation Metric: Area Under the ROC Curve (AUC)<br>
            Feature Importance: Assessed using permutation importance.
        </li>
    </ul>

    <div class="key-feature">
        <strong>Key Features</strong><br>
        • Race-Specific Analysis: Focus exclusively on non-Hispanic Black women.<br>
        • Nationally Representative Estimates: Use of NIS discharge weights.<br>
        • Integration of Clinical and Structural Determinants.<br>
        • Machine Learning–Driven Risk Prediction.<br>
        • Structural Inequity Gap: Quantifies mortality differences attributable to systemic factors.<br>
        • Regional Analysis: Highlights disparities across U.S. Census divisions.
    </div>

    <h2>Key Findings</h2>
    <div class="key-finding">
        <ul style="margin: 0; padding-left: 20px;">
            <li><strong>In-Hospital Mortality Rate:</strong> <span class="highlight">5.3%</span> among Black women.</li>
            <li><strong>Strongest Clinical Predictor:</strong> Metastatic disease (<span class="highlight">OR ≈ 2.18</span>).</li>
            <li><strong>Key Structural Predictors:</strong>
                <ul>
                    <li>Geographic Region: Highest risk in the <strong>Deep South (Division 6)</strong> and lowest in Division 8.</li>
                    <li>Insurance Status: Self-pay and Medicaid associated with higher mortality.</li>
                    <li>Socioeconomic Status: Lower ZIP income quartiles linked to increased risk.</li>
                    <li>Admission Type: Non-elective admissions significantly increase mortality.</li>
                </ul>
            </li>
            <li><strong>Structural Inequity Gap:</strong> Up to a <span class="highlight">37-percentage-point difference</span> in predicted mortality between high- and low-risk regions. A model‑based dashboard was created for user exploration of the inequity gap.</li>
        </ul>
    </div>

    <hr>

    <h1>Breast Cancer Mortality in Black Women – Datastory</h1>
    <div class="flourish-embed flourish-chart" data-src="story/3646484">
        <script src="https://public.flourish.studio/resources/embed.js"></script>
        <noscript>
            <img src="https://public.flourish.studio/story/3646484/thumbnail" width="100%" alt="visualization" />
        </noscript>
    </div>

    <h1>Breast Cancer Mortality in Black Women – Interactive Model Based Dashboard</h1>
    <div class="summary">
        <strong>Summary:</strong> Black women in the US experience disproportionately high breast cancer mortality. This model‑based dashboard visualizes structural inequity gaps based on data modelling from the 5,934 Black female cancer hospitalizations (2021 NIS): including in‑hospital mortality rate (5.3%), impact of metastatic disease (OR=2.18), and geographic/structural risk factors.
    </div>

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

    <div class="note">
        💡 <strong>User instructions:</strong> Hover over data points to see exact values. Use filters (if enabled) to explore by region, age, or socioeconomic strata.
    </div>
</div>
</body>
</html>
