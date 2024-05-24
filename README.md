
# Pharmacological Data Analysis

## Investigating The Pharmacodynamic And Pharmacokinetic Profiles Of A Drug Molecule

### The Project

**Description**
Pharmacological Data Analysis aims to understand how drugs work, their efficacy, safety, metabolism, and potential side effects using data generated during the first 2 phases of drug development (drug discovery & preclinical research). 

**Objective**
The primary objective is understanding:

- Relationships between the Compound X's properties, 
- Efficacy,
- Safety and
- Biological targets. 

Integrating and exploring multiple datasets in this project aims to uncover patterns and insights that can inform drug development and safety evaluations.


### The Dataset

**Overview**

- 3 datasets (Gene_Drug_Adverse_Event_Relationships.csv, Compound_Off_Target_Activity.csv and Project_Level_Data.csv)
- Almost 7 million rows across three datasets. 
- Features include gene symbol, adverse event, adverse event category, encoded adverse event category, compound ID, pic50, primary target assay bioactivity, molecular weight, cell permeability, compound solubility, fractional absorption, bioavailability, and clearance.


### The Process

- Data Integration
- Data Cleaning and Preprocessing
- Feature Selection & Engineering 
- Data Standardization
- Exploratory Data Analysis
- Statistical Analysis


### Data Cleaning and Preprocessing

- Dropping columns with unique values and > 50% missing values.
- Handling of missing values (Mean & Mode imputation)
- Removing duplicate rows 
- Removing outliers (IQR method) 
- Standardizing feature names
- Creating adverse event categories, encoding categorical features, combining columns 


### Exploratory Data Analysis

- Almost 2 million rows 
- Compound ID: 341
- Gene symbol: EGFR & PDGFRB
- Adverse Event Categories: hematological, dermatological, and cardiovascular. (17)
- Bioavailability: max value is 73.7%
- Fractional Absorption: max value 5.9
- Clearance: max value 41.2 (L/Hr/kg)
- Compound Solubility: max value is 705.0 (uM)
- Cell Permeability: max value is 85.0
- pIC50: max value is 6.4
- Primary Bioactivity: max value is 0.6
- Molecular Weight: max value is 453.5


### Exploring The Impact Of Physicochemical Properties On Bioavailability And Clearance


- Correlation Matrix showing relationships
- Key insights
1. ↑ Molecular Weight = ↓ Bioavailability and Clearance = ↓ Efficacy
2. ↑ Molecular Weight = ↓ Oral Bioavailability = ↓ Absorption
3. ↑ Molecular Weight = ↓ Clearance  = ↓ Safety 

Fig x: Physicochemical Properties vs Bioavailability and Clearance


###  Investigating The Relationship Between Primary Potency And Off-Target Activity

- Correlation Matrix showing relationships
- Key insights
1. ↑ Primary Target Assay Bioactivity = ↑ pIC50  = ↑ Efficacy
2. ↑ Primary Target Assay Bioactivity = ↑ pIC50  = ↑ Safety
3. ↑ Primary Target Assay Bioactivity = ↑ pIC50  = ↓ Metabolic Burden 

Fig x:  Assessing Primary Potency vs Selectivity 


### Is Higher Selectivity Directly Proportional To The Occurrence Of Fewer Adverse Events?

- Correlation Matrix showing relationships
- Key insights
1. ↑ pIC50 = ↓ Adverse Events = ↑ Efficacy
2. ↑ pIC50 = ↓ Adverse Events  = ↓ Dose 
3. ↑ pIC50 = ↓ Adverse Events  = ↑ Safety 

Fig x:  Drug Selectivity vs Adverse Reactions 


### Comparing In Vitro Bioactivity With In Vivo Intrinsic Clearance

- Correlation Matrix showing relationships
- Key insights
1. ↑ Primary Target Assay Bioactivity = ↓ Clearance   = ↑ Efficacy
2. ↑ Primary Target Assay Bioactivity = ↓ Clearance   = ↑ Dosing Duration
3. ↑ Primary Target Assay Bioactivity = ↓ Clearance   = ↓ Safety 


Fig x: In Vitro vs. In Vivo Properties


### Evaluating How Compound Solubility And Molecular Weight Affect Overall Fractional Absorption

- Correlation Matrix showing relationships
- Key insights
1. ↑ Molecular Weight = ↓ Compound Solubility = ↓ Fractional Absorption 
2. ↑ Molecular Weight = ↓ Compound Solubility = ↓ Fractional Absorption 
3. ↑ Molecular Weight = ↓ Compound Solubility = ↓ Fractional Absorption 


Fig x: Physicochemical Properties vs Absorption 


### Final Thoughts And Future Directions Based On Insights

**For Drug Development:**

- Focus on optimizing molecular weight and clearance for pharmacological profile optimization.

    
**For Further Research:**

- Apply machine learning algorithms to predict drug behavior, efficacy, and safety. 

1. Optimal criteria:  ↑ Bioavailability,  ↑ Fractional Absorption, ↑ Compound Solubility,  ↑ Cell Permeability, ↑ pIC50, ↑ Primary Bioactivity, Moderate Clearance and Molecular Weight values. 
2. New target feature creation (defining a function for the optimal criteria).
3. Model training and prediction
4. Evaluating model performance
5. Rank optimal compounds

-  Validate findings with additional in vivo studies.

### Dependencies

- Python
- Seaborn
- Mathplotlib
- Numpy
- Pandas
- Bokeh
- SKLearn

