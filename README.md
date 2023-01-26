
![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white) ![Microsoft SharePoint ](https://img.shields.io/badge/Microsoft_SharePoint-0078D4?style=for-the-badge&logo=microsoft-sharepoint&logoColor=white)

# Sanitation KPIs in a Plant-based meat manufacturing plant

An environmental monitoring program (EMP) is an operation-specific program that helps to assess the **effectiveness of sanitation practices** through pathogen swabbing. It ensures the food safety programs in place are not only verified, but also validated to ensure the food safety programs limit or eliminate risk-based pathogens that could potentially cause harm to consumers. It is part of SQF, FSSC 22000 and HACCP.

The objective of this project is to set up a system that allows to record and analyze microbiological swabs as part of the food safety program.

## The Challenge

The number of microbiological swabs in a 45,000 sq. ft facility is big. The swabs also need to be traceable to the site of swabbing, time and day. Therefore, as part of a team building a QMS (Quality Management System) from the ground up, a system to log and analyze swabs was needed.

## The Opportunity

The opportunity to develop an environmental monitoring program that can be used to make data driven decisions not only benefits the customer with a robust food safety program, it also benefits the organization because an EMP is a fundamental element of GFSI certifications. GFSI certifications such as SQF are trusted by retailers around the world. It helps give the organization status and opens doors for future business and growth.

## Methodology

### EMP Design

Total swabs + air sampling in a month: 261

![](https://github.com/aleivaar94/Excel-Sanitation-KPI/blob/master/assets/emp-design.png)

### Data Collection

### **Part I**
Due to the high number of swabs a data collection solution was necessary. In this case a Microsoft Form was created. Automatic data collection in MS Form and Excel allows ease of laboratory swab submission considering the high number of swabs. It also allows data analysis and minimizes errors while submitting lab samples to the lab (wrong sample name or missed swab).

Rooms have a code that identify in which location the swab was taken, providing a level of traceability. For example: KE= Kettle Room.

- The Julian Date provides traceability to the year and day. The form automatically logs the time of swab.
- The type of swab and equipment are identified as well.
- The form also allows to submit pictures.

### **Part II**

Data is submitted and collected in a Microsoft Excel linked to the Microsoft Form. The Excel spreadsheet has an **algorithm** that concatenates values to provide a name nomenclature depending on the type of swab submitted.

For an "Equipment" type of swab: Julian Date – Equipment name – Swabbed Area Description – Zone – Swab #

- Example: **21721-CC215-Blue conveyor-Z1-5**

For an "Air/Drain/Floor/Corner/Wall" type of swab: Julian Date - Room - Type (Air/Drain) - Zone – Swab #

- Example: **21721-SC-Drain-Z3-8**

For a "Hand Swab/Hose" type of swab: Julian Date - Type (Hand Swab/Hose) - Swab #

- Example: **21721-Hand Swab-8**


![](https://github.com/aleivaar94/Excel-Sanitation-KPI/blob/master/assets/data-collection-form.png)


### Data Cleaning

Equipment names were standardized, for example, bucket plastic, Bucket plastic -> Bucket (Plastic), bucket SS or Bucket stainless steel -> Bucket (SS). This is critical because the equipment needs to have the same name to analyse and compare results per month. Equipment name and Rooms are reviewed and cleaned every round as new equipment or tools are added depending on the business needs or when submission mistakes are made.

![](https://github.com/aleivaar94/Excel-Sanitation-KPI/blob/master/assets/swab-lab-submission.png)


### Data Analysis

Due to high variability of results in parameters like ACC, Yeast and Mould, an average of CFU/swab can’t be performed. Therefore, the results are grouped in “bins” with a range of 100 CFU/swab per bin. This means that CFU/swab results are grouped per these ranges and the values that fall within these ranges are counted, creating a frequency. Results were analysed with the help of pivot tables and pivot charts.

![](https://github.com/aleivaar94/Excel-Sanitation-KPI/blob/master/assets/z1-indicators.png)

<br>

![](https://github.com/aleivaar94/Excel-Sanitation-KPI/blob/master/assets/z2-indicators.png)

<br>

![](https://github.com/aleivaar94/Excel-Sanitation-KPI/blob/master/assets/z3-listeria.png)


## Results

- Sanitation practices appear to be improving due to the decrease in indicator organisms in subsequent months.
- Z4 has a low count of E. coli & Total coliforms (<10 or below limit of detection). This indicates we have good hand washing as part of GMP.
- EMP should be performed after cleaning and sanitation procedures. Preferably at a fixed time that allows for a “reset” in production cycle.
- While Listeria POSITIVES haven’t surfaced in September, there needs to be more data to conclude that the updated Drain sanitation procedure is effective. Listeria POSITIVES belong to Drains and none have appeared in Hoses as per the EMP design.

## Future Work

- The different number of swabs per round, different rounds, different swab locations and different times confound results.
- Number of swabs could be reduced and a blueprint of approximate 2 equipment swabbing locations with the most difficult to clean locations per zone 1 and 2 could be considered. The EMP should have an approach to seek and destroy. This will minimize other factors affecting the data analysis and make it faster and easier to analyse for meaningful call to actions.