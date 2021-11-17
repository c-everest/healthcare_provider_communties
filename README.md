# Using Healthcare Provider Communities to Identify Strategic Growth Opportunities for Hospital Systems

### Project overview
This project identifies market growth opportunities at a hospital system level by exploring how Medicare patients move through the Middle Tennessee healthcare system using referral patterns from healthcare providers to Nashville area acute care hospitals.  For two weeks we worked in small teams, after which all 17 [members](https://sites.google.com/view/nashvilleprovidersds4/references) of the cohort collaborated to weave key insights from our groups into a cohesive narrative.  The final presentation was delivered to the VP of Data Science & Analytics for Healthcare Bluebook, Mikil Taylor. Mikil’s feedback on the project can be found [here](https://world.hey.com/mikil/the-best-presentation-i-ve-ever-seen-cc11b0b9).  

### Objectives
* Create a profile of healthcare providers referring Medicare patients to the major hospitals in Nashville.  Are certain specialties more likely to refer patients to a particular hospital?
* Determine which providers Vanderbilt Hospital should reach out to in the Nashville area in order to increase patient volume.
* Research which providers send significant numbers of patients only to Vanderbilt’s competitor hospitals, such as TriStar Centennial Medical Center.
* If Vanderbilt wants to increase patient volume, in what areas of specialty care do they have room for growth?
* dentify provider communities in the Nashville-Davidson County CBSA, making use of the Louvain community detection [algorithm](https://neo4j.com/docs/graph-data-science/current/algorithms/louvain/). 

### Presentation
https://sites.google.com/view/nashvilleprovidersds4/home

### Results
We took the dataset of just over 6K unique Nashville providers and general acute care hospitals and ran the Louvain community detection algorithm. We determined that each community of providers revolves primarily around one hospital. We used the zip code of the provider office locations and generated a heatmap of the communities of Medicare recipients each hospital serves. The analysis revealed that providers-hospital communities are dominated by three major hospital systems and fall into geographic clusters but the zip codes are served at different intensities. <br />

An inherent limitation of the Hop Teaming dataset is that the patient population includes only Medicare benificiaries.  This largely precluded us from exploring hospital growth opportunities in certain areas such as plastic surgery, sports medicine or pediatrics.  With this in mind, I leveraged additional [data](https://www.cms.gov/Research-Statistics-Data-and-Systems/Statistics-Trends-and-Reports/Chronic-Conditions) from the Centers for Medicare & Medicaid Services and analyzed the most prevalent chronic conditions among Medicare benificiaries as well as common comorbidities.  Conditions like Ischemic Heart Disease and Chronic Obstructive Pulmonary Disease that involve the cardiac and pulmonary systems account for 7 out of the 21 chronic conditions identified as driving the most spend by Medicare.  While Vanderbilt dominated patient referral volume in areas like Family Medicine and Internal Medicine, I revealed significant opportunity for Vanderbilt to significantly increase market share of referrals in pulmonary and cardiac subspecialties.

![](/images/cardiac_pulmonary_market_opp.png)


### Data
* 2017 Hop Teaming [dataset](https://careset.com/datasets-3/), illustrating the healthcare ecosystem and patient sharing relationships among Medicare providers 
* National Plan and Provider Enumeration System (NPPES) Data [Dissemination](https://download.cms.gov/nppes/NPI_Files.html)
* National Uniform Claim Committee healthcare provider taxonomy [crosswalk](https://www.nucc.org/index.php/code-sets-mainmenu-41/provider-taxonomy-mainmenu-40/csv-mainmenu-57)
* Core-Based Statistical Area (CBSA) to zip code [crosswalk](https://www.huduser.gov/portal/datasets/usps_crosswalk.html)

### Team
* Courtney Everest (team lead)
* Armelle Le Guelte
* Alexa Zylstra
