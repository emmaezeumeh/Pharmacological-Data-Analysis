![image](https://github.com/emmaezeumeh/Pharmacological-Data-Analysis/assets/115907457/ce339ca2-7f74-4a2b-aa4e-1cbab5cdef1c)


# Pharmacological Data Analysis

## Investigating The Pharmacodynamic And Pharmacokinetic Profiles Of Drug Compounds


### The Project

**Description**
Pharmacological Data Analysis aims to understand how drugs work, their efficacy, safety, metabolism, and potential side effects using data generated during the first 2 phases of drug development (drug discovery & preclinical research). 

**Objective**
The primary objective is understanding:

- Relationships between the Compounds' properties, 
- Efficacy and
- Safety. 

Integrating and exploring multiple datasets in this project aims to uncover patterns and insights that can inform drug development and safety evaluations.


### The Dataset

**Overview**

- 3 datasets (Gene_Drug_Adverse_Event_Relationships.csv, Compound_Off_Target_Activity.csv and Project_Level_Data.csv)
- Almost **7 million** rows across three datasets. 
- Features include encoded adverse event category, pic50, primary target assay bioactivity, molecular weight, cell permeability, compound solubility, fractional absorption, bioavailability, and clearance.

**Histograms Showing Feature Distribution**

![image](https://github.com/emmaezeumeh/Pharmacological-Data-Analysis/assets/115907457/7d7a0585-8b12-44ed-abc3-01db560b86ec)


### The Process

- Data Integration
- Data Cleaning and Preprocessing
- Feature Selection & Engineering 
- Exploratory Data Analysis
- Statistical Analysis


### Data Cleaning and Preprocessing

- Dropping columns with unique values.
- Removing duplicate rows 
- Transformation of features (Log)
- Handling of missing values (Mean & Mode imputation)
- Standardizing feature names
- Creating adverse event categories, encoding categorical features, combining columns 

**Histograms Showing Feature Distribution After Log Transformation**
  
![image](https://github.com/emmaezeumeh/Pharmacological-Data-Analysis/assets/115907457/f7e50037-f4cb-4d45-a73d-66c5d6275432)

### Features of Interest

- **Compound ID**: A unique code given to a specific chemical compound or drug being studied.
- **Adverse Event**: Any unwanted or harmful effect after taking a drug or compound.
- **Adverse Event Category**: Groups the adverse events into larger categories based on the system they affect in the body.
- **Adverse Event Category Encoded**: A number assigned to each adverse event category to facilitate analysis.
- **Bioavailability**: The proportion of a compound that reaches the bloodstream after it is introduced into the body. 
- **Fractional Absorption**: The percentage of a compound absorbed into the bloodstream.
- **Intrinsic Clearance (L/Hr/kg)**: The rate at which a compound is broken down and eliminated from the body by the liver.
- **Compound Solubility (uM)**: Measures how much a compound can dissolve in a given solvent. 
- **Cell Permeability**: Measures how easily a compound can pass through cell membranes. 
- **pIC50**: A measure of the potency of a compound. 
- **Primary Bioactivity**: A measure of the overall biological effect of a compound on its intended biological target.
- **Molecular Weight**: The total weight of a compound/drug molecule.


### Exploratory Data Analysis

- Almost **3 million** rows 
- **Compound ID:** 341
- **Top 3 Adverse Event Categories:** Haematological, Dermatological, and Cardiovascular.
- **Positive Correlation:**
  
  log_fafg_rat and log_bioavailability_rat,
  
  log_primary_bioactivity and log_molecular_weight, &
  
  log_compound_solubility_um and log_fafg_rat
  
- **Negative Correlation:**
  
  log_molecular_weight and log_cell_permeability,
  
  log_molecular_weight and log_compound_solubility_um, &
  
  log_primary_bioactivity and log_clint_rat_l_hr_kg

**Correlation Matrix of Transformed Features**

![image](https://github.com/emmaezeumeh/Pharmacological-Data-Analysis/assets/115907457/f43eb234-eaeb-463a-950f-7b29dd25244f)


### Exploring The Impact Of Physicochemical Properties On Clearance

- **Key insights**
1. ↑ Log of Molecular Weight = ↓ Log of Clearance = ↓ Efficacy
2. ↑ Log of Molecular Weight = ↓ Log of Clearance  = ↓ Safety 


![image](https://github.com/emmaezeumeh/Pharmacological-Data-Analysis/assets/115907457/ea5bf165-6ea1-4f8c-a8f0-e2ce23090bc8)


###  Investigating The Relationship Between Primary Potency And Off-Target Activity

- **Key insights**
1. ↑ Log of Primary Target Assay Bioactivity = ↑ pIC50  = ↑ Efficacy
2. ↑ Log of Primary Target Assay Bioactivity = ↑ pIC50  = ↑ Safety

![image](https://github.com/emmaezeumeh/Pharmacological-Data-Analysis/assets/115907457/e7f95e9c-8a71-4990-83bc-0341c782b1ec)


### Is Higher Selectivity Directly Proportional To The Occurrence Of Fewer Adverse Events?

- **Key insights**
1. ↑ pIC50 = ↓ Adverse Events = ↑ Efficacy & Safety
2. ↑ pIC50 = ↓ Adverse Events  = ↓ Dose 

![image](https://github.com/emmaezeumeh/Pharmacological-Data-Analysis/assets/115907457/318f65d0-a2f6-484a-9753-cbe8b4e3c282)


### Comparing In Vitro Bioactivity With In Vivo Intrinsic Clearance

- **Key insights**
1. ↑ Log of Primary Target Assay Bioactivity = ↓ Log of Clearance   = ↑ Efficacy
2. ↑ Log of Primary Target Assay Bioactivity = ↓ Log of Clearance   = ↓ Safety 

![image](https://github.com/emmaezeumeh/Pharmacological-Data-Analysis/assets/115907457/4ec7a6db-5aa5-4cab-8728-2ee346946e92)


### Evaluating How Compound Solubility And Molecular Weight Affect Overall Fractional Absorption

- **Key insights**
1. ↑  Log of Molecular Weight = ↓  Log of Compound Solubility 
2. ↑  Log of Molecular Weight = ↓  Log of Fractional Absorption 
3. ↑  Log of Compound Solubility = ↑  Log of Fractional Absorption  

![image](https://github.com/emmaezeumeh/Pharmacological-Data-Analysis/assets/115907457/0072484f-f3f8-4f59-b6f7-f56e41b373a6)


### Final Thoughts And Future Directions Based On Insights

**For Further Research:**

- Focus on optimizing molecular weight and clearance for pharmacological profile optimization.
- Apply machine learning algorithms to predict drug behavior, efficacy, and safety. 

1. Optimal criteria:

   ↑ Bioavailability,
   
   ↑ Fractional Absorption,
   
   ↑ Compound Solubility,
   
   ↑ Cell Permeability,
   
   ↑ pIC50,
   
   ↑ Primary Bioactivity,
   
   Moderate Clearance and Molecular Weight values.
    
3. New target feature creation (defining a function for the optimal criteria).
4. Model training and prediction
5. Evaluating model performance
6. Rank optimal compounds

-  Validate findings with additional in vivo studies.


### Dependencies

- Python
- Seaborn
- Mathplotlib
- Numpy
- Pandas

