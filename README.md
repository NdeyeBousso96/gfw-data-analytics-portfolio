**<h1 align="center">Portfolio Data Analytics with Global Fishing Watch</h1>**

**<h2 align="center">Exploring Fishing Activity in Member Countries of the Sub-Regional Fisheries Commission (SRFC) and the Fisheries Committee for the West Central Gulf of Guinea (FCWC)</h2>**

**<h2 align="center">Author: Ndeye Coumba Bousso</h2>**

### **Overview**

This portfolio explores the variation of fishing activity in member countries of the Sub-Regional Fisheries Commission (CSRP/SRFC) and the Fisheries Committee for the West Central Gulf of Guinea (CPCO/FCWC) across key parameters, including year and month, flag state, gear type, and Marine Protected Areas (MPAs). The analysis covers the period from 2020 to 2024. The SRFC (CSRP in French) member states are Senegal, Mauritania, The Gambia, Guinea-Bissau, Guinea, Sierra Leone, and Cabo Verde, while the FCWC (CPCO in French) member states are Benin, Côte d’Ivoire, Ghana, Liberia, Nigeria, and Togo.

This portfolio explores Global Fishing Watch data to answer key questions, such as :

•	How does the total number of fishing hours vary by year and by fleet type (local vs. foreign) in the areas covered by the CSRP and the CPCO? How does this variation look for each individual CSRP and CPCO member country?

•	Which are the top five flag states with the highest total fishing hours in the CSRP and CPCO regions? Which are the top five flag states in each individual CSRP and CPCO member country?

•	How does the total number of fishing hours vary by gear type in the CSRP and CPCO regions? What are the five most commonly used fishing gear types in each CSRP and CPCO country?

•	What are the top five most used fishing gear types by the top five flag states with the highest total fishing hours in the CSRP and CPCO regions?

•	How does the total number of fishing hours vary by month in the CSRP and CPCO regions? How does this monthly variation appear for each CSRP and CPCO country?

•	How do fishing hours using trawler gear vary by month in each CSRP and CPCO country?

•	What are the total fishing hours recorded within Marine Protected Areas (MPAs) in the CSRP and CPCO regions?

### **Data Sources**

•	**Global Fishing Watch** : Vessel activity and fishing hours (2020–2024)  
*[Global Fishing Watch](https://globalfishingwatch.org/ ). 2025. Global Apparent Fishing Effort Dataset, Version 3.0. doi:10.5281/zenodo.14982712*

•	**Marine Regions** : Exclusive Economic Zones (EEZs) layers  
*Flanders Marine Institute (2023). Maritime Boundaries Geodatabase: Maritime Boundaries and Exclusive Economic Zones (200NM), version 12. Available online at http://www.marineregions.org/ . https://doi.org/10.14284/632  (look up in IMIS)*

•	**Protected Planet** : World Database on Protected Areas (WDPA), Marine Protected Areas shapefiles  
*UNEP-WCMC and IUCN (2025), Protected Planet: The World Database on Protected Areas (WDPA) and World Database on Other Effective Area-based Conservation Measures (WD-OECM) [Online], July 2025, Cambridge, UK: UNEP-WCMC and IUCN. Available at: www.protectedplanet.net.* 

### **Tools and Technologies**

•	**BigQuery** : Data processing and aggregation

•	**SQL** : Querying and aggregating large datasets

•	**Tableau** : Data analysis and visualization

•	**R** : Data analysis and visualization

•	**QGIS** : Spatial data processing

•	**PowerPoint** : Presentation of figures and insights

•	**ChatGPT**: acting as a conversational AI, for conceptualization, coding assistance and narrative support. All analysis, decisions, and interpretations were my own.

### **Methodology**

The full methodology is detailed in:
[Methodology Document](Methodology_Portfolio_GlobalFishingWatch_NdeyeBousso.docx).
**Note**: The Methodology Document is provided in Word format (.docx) to ensure that all spatial data (including multipolygon data) and comments are fully visible.

Key Steps:

1.	Aggregate Global Fishing Watch data (2020–2024) using SQL.

2.	Extract EEZ spatial data for each country using SQL.

3.	Classify fishing flags as foreign or local using SQL.

4.	Filter data for trawler fishing activity using SQL.

5.	Group trawler fishing hours by country and month using SQL.

6.	Filter MPAs shapefiles in QGIS.

7.	Convert WKT columns from STRING to GEOGRAPHY type in BigQuery.

8.	Tag fishing data with MPA names using SQL

9.	Aggregate fishing hours by fleet, flag, gear, country, and month using Tableau.

10.	Analyze data and create visualizations in Tableau.

11.	Analyze data and create visualizations in R.

### **Key Findings**

Figures and summarized findings are presented in: 
[Figures and Findings Presentation](Figures_Findings_Portfolio_GlobalFishingWatch_NdeyeBousso.pdf).
The same figures visualizations are also available on Tableau: 
[View Tableau Visualizations](https://public.tableau.com/app/profile/ndeye.coumba.bousso/viz/Tableau_Visualizations_Portfolio_GlobalFishingWatch_NdeyeBousso ).

1.	**Total Fishing Hours in CSRP/SRFC Member States by Year and Fleet Type**
(Aggregated effort from Cabo Verde, Gambia, Guinea, Guinea-Bissau, Mauritania, Senegal, and Sierra Leone  
**Definition**: Local vessels are those flying the flag of a CSRP member state (CPV – Cabo Verde, MRT – Mauritania, SEN – Senegal, GMB – The Gambia, GNB – Guinea-Bissau, GIN – Guinea, and SLE – Sierra Leone). Any vessel with a flag different from these is classified as a foreign vessel.  
**Observation**: Across all five years, fishing activity in the combined CSRP member states is predominantly carried out by foreign vessels—approximately twice as much as by local vessels.  

2.	**Total Fishing Hours in CPCO/FCWC Member States by Year and Fleet Type**
(Aggregated effort from Benin, Côte d’Ivoire, Ghana, Liberia, Nigeria, and Togo)  
**Definition**: Local vessels are those flying the flag of a CPCO member state (BEN – Benin, CIV – Côte d’Ivoire, GHA – Ghana, LBR – Liberia, NGA – Nigeria, and TGO – Togo). Any vessel with a flag different from these is classified as a foreign vessel.  
**Observation**: In all years except 2020, fishing activity in the combined CPCO member states is predominantly carried out by local vessels—about 2 to 4 times more than by foreign vessels.  

3.	**Total Fishing Hours per CSRP/SRFC Country by Year and Fleet Type**  
When examining fishing hours by member country:  
•	**Cabo Verde, Guinea-Bissau, and Mauritania**: Foreign vessels account for the majority of fishing activity in all five years, while local vessels contribute less.  
•	**Gambia and Senegal**: Local vessels account for the majority of fishing activity in all years, with foreign vessels contributing a smaller share.  
•	**Sierra Leone**: The predominance shifts over time — foreign vessels lead in 2021 and 2022, while local vessels take the lead in 2023 and 2024.  
•	**Guinea**: Foreign vessels dominate in all years except 2020.  

4.	**Total Fishing Hours per CPCO/FCWC Country by Year and Fleet Type**  
•	**Liberia**: Fishing activity is consistently dominated by foreign vessels across all five years, whereas in **Ghana**, local vessels are predominant.  
•	**Côte d’Ivoire**: Foreign vessels dominate in all years except 2020, while in **Nigeria**, local vessels are mostly in the lead.  
•	**Benin**: Local vessels predominate in all years except 2023.  
•	**Togo**: The predominance shifts over time: foreign vessels are more active from 2020 to 2022, while local vessels take the lead in 2023 and 2024.  

5.	**Top 5 Flag States by Total Fishing Hours in CSRP/SRFC and CPCO/FCWC Member States**  
•	Combined CSRP member states: Fishing is mostly carried out by vessels flagged in **China (CHN), Senegal (SEN), Spain (ESP), Mauritania (MRT)**, and **Guinea-Bissau (GNB)**.  
•	Combined CPCO member states: Fishing is mostly carried out by vessels flagged in **Nigeria (NGA), UNKNOWN-NGA, Ghana (GHA), China (CHN)**, and **Senegal (SEN)**.  

6.	**Top 5 Flag States by Total Fishing Hours per CSRP/SRFC Country**  
•	**Cabo Verde**: Fishing is mostly carried out by vessels flagged in **Spain (ESP)**.  
•	**Senegal and Gambia**: Fishing is mostly carried out by vessels flagged in **Senegal (SEN)**.  
•	**Guinea and Guinea-Bissau**: Fishing is mostly carried out by vessels flagged in **China (CHN)**.  
•	**Mauritania**: Fishing is mostly carried out by vessels flagged in **China (CHN)**, except in 2024 when **Spain (ESP)** accounts for the highest fishing activity.  
•	**Sierra Leone**: From 2020 to 2022, the flag of **Senegal (SEN)** predominates, while in 2023 and 2024, the flags of **Spain (ESP)** and **China (CHN)** predominate, respectively.  

7.	**Top 5 Flag States by Total Fishing Hours per CPCO/FCWC Country**  
•	**Ghana and Togo**: Fishing is mostly carried out by vessels flagged in **Ghana (GHA)**.  
•	**Liberia**: The flag of **China (CHN)** predominates.  
•	**Nigeria**: The flag of **Nigeria (NGA)** predominates, except in 2020 when UNKNOWN-NGA predominates.  
•	**Benin**: From 2020 to 2021, the flag of **Ghana (GHA)** predominates, while from 2022 to 2024, the flag of **Nigeria (NGA)** predominates.  
•	**Côte d’Ivoire**: From 2021 to 2023, the flag of **China (CHN)** predominates, while in 2020 and 2024, the flag of **Ghana (GHA)** predominates.  

8.	**Total Fishing Hours in CSRP/SRFC Member States by Gear Type**  
**Combined CSRP member countries**: Over the five-year period, **trawlers** were by far the most widely used fishing gear.  

9.	**Total Fishing Hours in CPCO/FCWC Member States by Gear Type**  
**Combined CPCO member countries**: Over the five-year period, **trawlers** were by far the most widely used fishing gear, with total fishing effort increasing over the years.  

10.	**Top 5 Most Used Fishing Gear Types by Total Fishing Hours per CSRP/SRFC Country**  
•	**Gambia, Guinea, Guinea-Bissau, Mauritania, and Senegal**: Over the five-year period, **trawlers** were by far the most widely used fishing gear.  
•	**Cabo Verde**: Over the five-year period, **drifting longlines** were by far the most widely used fishing gear.  
•	**Sierra Leone**: From 2021 to 2023, **tuna purse seines** were the most used fishing gear, while in 2020 and 2024, **trawlers** predominated.  

11.	**Top 5 Most Used Fishing Gear Types by Total Fishing Hours per CPCO/FCWC Country**  
•	**Nigeria, Togo, Liberia, and Ghana**: Over the five-year period, **trawlers** were the most used fishing gear.  
•	**Côte d’Ivoire**: **Tuna purse seines** were the most used fishing gear, except in 2020 when **trawlers** predominated.  
•	**Benin**: In 2020, **pole and line** were the most used fishing gear, in 2021 **tuna purse seines** predominated, and from 2022 to 2024, **trawlers** were by far the most widely used fishing gear.  

12.	**Top 5 Fishing Gear Types Used by the Top 5 Flag States with the Highest Total Fishing Hours in CSRP/SRFC Countries**  
**Top five flag states in the CSRP area**: **China (CHN), Spain (ESP), Guinea-Bissau (GNB), Mauritania (MRT)**, and **Senegal (SEN)** mainly used **trawlers** as fishing gear over the five-year period.  

13.	**Top 5 Fishing Gear Types Used by the Top 5 Flag States with the Highest Total Fishing Hours in CPCO/FCWC Countries**  
**Top five flag states in the CPCO area**: Four flags—**China (CHN), Ghana (GHA), Nigeria (NGA), and UNKNOWN-NGA**—mainly used **trawlers** as fishing gear over the five-year period. The remaining flag, **Senegal (SEN)**, mainly used **trawlers** from 2021 to 2022, while in 2020, 2023, and 2024, **tuna purse seines** were most used.  

14.	**Total Fishing Hours in CSRP/SRFC Member States by Month**  
**CSRP area (2020–2024)**: Among the months, **August** was often associated with the highest fishing activity.  

15.	**Total Fishing Hours in CPCO/FCWC Member States by Month**  
**CPCO area (2020–2024)**: The month with the highest fishing activity generally fell between **June and December**.  

16.	**Total Fishing Hours per CSRP/SRFC Country by Month**  
**CSRP member countries (2020–2024)**: In each country, the month with the highest fishing activity varied across the different years, except in **Senegal**, where it was almost always **August**.  

17.	**Total Fishing Hours per CPCO/FCWC Country by Month**  
**CPCO member countries (2020–2024)**: In each country, the month with the highest fishing activity varied across the different years, except in **Ghana**, where it was almost always **June**.  

18.	**Monthly Fishing Hours with Trawlers in CSRP/SRFC Member States (2020–2024)**  
•	CSRP member countries combined (2020–2024): The **maximum trawler fishing activity** generally occurred between **July and September**, except in 2020 when it was **March**. Within this interval, **September** most frequently recorded the **highest trawler fishing hours**.  
•	Conversely, **November** usually had the **lowest trawler fishing hours**, except in 2023 when **January** recorded the **minimum**.  

19.	**Monthly Fishing Hours with Trawlers in CPCO/FCWC Member States (2020–2024)**  
•	CPCO member countries combined (2020–2024): The **highest trawler fishing hours** occurred in either **October** or **December**.  
•	Conversely, the **lowest trawler fishing hours** generally fell between **February and March**.  

20.	**Total Fishing Hours in CSRP/SRFC Marine Protected Areas (MPAs)**  
The table presents **MPAs** within the area covered by CSRP that have recorded data in the Global Fishing Watch dataset. Some MPAs have point coordinates appearing in the dataset but are associated with **zero fishing hours**. The MPAs with the **highest fishing hours** are **Gorée** in Senegal, followed by **Bolama–Bijagos** and **Ilhas Formosa, Nago & Tchedia (Urok)** in Guinea Bissau. Among CSRP member countries, MPAs in **Mauritania, Gambia, and Guinea** have no recorded data in the Global Fishing Watch dataset, corresponding to **zero fishing hours**.  

21.	**Total Fishing Hours in CPCO/FCWC Marine Protected Areas (MPAs)**  
There are **no recorded data** in the Global Fishing Watch dataset for MPAs within the area covered by CPCO, resulting in **zero fishing hours**. MPAs in **Côte d’Ivoire, Liberia, and Nigeria** show **zero fishing activity**. For **Benin, Ghana, and Togo**, no MPAs are listed in the World Database on Protected Areas from the Protected Planet website.  

### **Acknowledgements**  

This portfolio was supported by Global Fishing Watch for making their dataset publicly available, and by conversational AI tools (ChatGPT) for conceptualization, code review, and narrative guidance. All analysis, decisions, and interpretations were independently performed by the author.
