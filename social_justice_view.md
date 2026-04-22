# Social Justice and Ethical Advocacy  
## The Structural Determinants of In‑Hospital Breast Cancer Mortality Among Black Women

### Problem Statement

**The Population**  
This analysis centers on **non‑Hispanic Black women** hospitalized with breast cancer in the United States. Despite overall declines in cancer mortality, this group continues to experience a persistent, unjust survival disadvantage.

**The Injustice**  
For over a decade, Black women have died from breast cancer at a rate **41% higher** than White women, even as diagnosis rates have nearly equalized (ACS, 2023). The prevailing narrative often attributes this gap to “biological differences” or individual behaviors. However, a growing body of evidence points to structural forces, insurance type, neighborhood socioeconomic status, geographic region, and admission patterns as independent drivers of mortality. This study investigates a specific, under‑examined site of inequity: in‑hospital death. When a Black woman with breast cancer is admitted to a hospital, her risk of dying during that stay should not be dictated by her zip code or insurance card. Yet our data show otherwise.

**Literature Review (Three Credible Sources)**  
1. Hardy & Du (2021) analyzed 547,703 women in SEER (2007‑2016) and found that African American women presented with larger tumors (≥4 cm: 20.6% vs. 14.1%), later stage at diagnosis, and higher all‑cause mortality (HR=1.18) after full adjustment. Critically, even after controlling for clinical factors, racial disparities persisted, pointing to unmeasured structural barriers.  
2. DeSantis et al. (2017) documented that Black‑to‑White breast cancer mortality ratios vary from 1.0 in some states to >2.0 in the Deep South. This geographic variation cannot be explained by biology alone; it reflects differential access to screening, timely treatment, and high‑quality oncology care.  
3. Collin et al. (2022) studied 6,011 women in metropolitan Atlanta and found Black women were twice as likely to experience surgical delay >30 days (OR=2.15). Delay >60 days was associated with a 28% increase in breast cancer mortality. Racial disparities in mortality were smallest at government facilities (HR=1.31) and largest at non‑profit facilities (HR=2.11), demonstrating that institutional context mediates structural injustice.

These studies collectively establish that race is not a biological risk factor but a social one but a marker of differential exposure to structural barriers.

### The Findings: Evidence from the NIS 2021 Analysis

**Connecting to Our Analysis**  
We analyzed **5,934 hospitalizations** of Black women with breast cancer from the 2021 National Inpatient Sample (NIS). Using a machine learning framework (Logistic Regression; Elastic Net, AUC = 0.69), we identified the strongest predictors of in‑hospital mortality:

- **Clinical severity** – Metastatic disease carried an odds ratio of **2.18**, confirming that advanced cancer is the dominant clinical driver.  
- **Structural factors** – Even after adjusting for metastatic disease, the following independently predicted mortality:  
  - **Geographic region**: Division 6 (South: AL, KY, MS, TN) showed the highest risk; Division 8 (CO, AZ) the lowest.  
  - **Insurance status**: Self‑pay and Medicaid patients had significantly higher mortality than those with private insurance.  
  - **Socioeconomic status**: Lower ZIP code income quartiles were linked to increased risk.  
  - **Admission type**: Non‑elective (emergency) admissions dramatically raised mortality odds.

**The Reality Check**  
Our findings confirm the existence of a **structural inequity gap**. A 60‑year‑old Black woman with metastatic disease, private insurance, low income, and CHF faces an **88% predicted in‑hospital mortality** if treated in the Deep South. The same patient with the exact same clinical profile would have only **51% predicted mortality** if treated in Division 8. That is a **37‑percentage‑point difference** – a gap driven entirely by geography, not by her cancer.  

This finding refutes the notion that Black women’s higher mortality is simply a matter of later stage at diagnosis. Even when clinical severity is held constant, **where** a patient is treated and **how** she accesses care (Location, insurance, elective vs. emergency admission etc.) profoundly shape survival. The model‑based dashboard we built allows users to explore this inequity in real time.

**Bias Check – Limitations of Our Data**  
While the NIS is nationally representative, it has inherent biases:  
- **Inpatient only** – We cannot capture deaths that occur after discharge or in hospice. Our findings generalize only to hospital stays.  
- **Missing variables** – The NIS does not include data on hospital quality (e.g., nurse‑to‑patient ratios, oncology certification), patient navigation, or direct measures of racism (e.g., discrimination in triage). These unmeasured confounders may partially explain the regional and insurance effects we observe.  
- **Coding bias** – ICD‑10 codes for comorbidities may be under‑reported, especially for Black patients who historically receive less thorough documentation (a form of measurement bias).  
- **Survivorship bias** – Patients who die before reaching a hospital are absent from the dataset. This likely *underestimates* the true disparity, because barriers to care (lack of insurance, rural location) prevent some women from ever being admitted.

Thus, our reported structural inequity gap of 37 percentage points is likely a **conservative estimate** of the true social injustice.

### Advocacy & Recommendations: A Call to Action

**What Needs to Change**  
Data without action is merely academic. Our analysis points to three concrete policy and practice shifts:

1. **Geographic investment in high‑mortality regions** – The South (Division 6) requires targeted funding for breast cancer navigation programs, mobile mammography, and Medicaid expansion. States that have not expanded Medicaid (e.g., Alabama, Mississippi) leave Black women without coverage, forcing them to present as self‑pay or through emergency admissions – both of which our model identifies as lethal risk factors.

2. **Insurance as a structural intervention** – Our finding that self‑pay and Medicaid patients have higher mortality even after adjusting for disease severity demands that hospitals implement **universal patient navigation** for all uninsured/underinsured breast cancer patients. Navigators can convert non‑elective admissions to elective, schedule timely surgery, and connect patients to financial assistance.

3. **Data infrastructure for equity monitoring** – The NIS should collect race‑stratified, hospital‑level quality metrics (e.g., time from diagnosis to treatment, receipt of guideline‑concordant care). Without these variables, researchers cannot fully hold institutions accountable.

**Human Impact of Inaction**  
Every percentage point of the structural inequity gap represents real lives. A 37‑point gap means that for every 100 Black women with metastatic breast cancer in the Deep South, roughly **37 more will die** than if they received care in a lower‑risk region – not because their tumors are different, but because the system failed them. Inaction perpetuates the 41% excess mortality that has persisted for decades.  

We owe it to the 5,934 women in this study and to the thousands who will be hospitalized next year to stop treating structural inequity as an unfortunate fact and start treating it as an urgent, solvable crisis.

---

*“Behind every row in this dataset is a human story and behind the structural inequity gap is a system that can choose to change.”*
