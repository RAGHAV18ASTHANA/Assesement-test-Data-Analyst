Data-Quality Issues & Analytical Risks1. Negative Billing Amounts   
How it affects analysis: 108 records showed negative values . Leaving these in would artificially deflate total hospital revenue and skew average cost metrics.   
How handled: Applied absolute values (abs()) during Python data cleaning to convert these into positive charges.   
2. Synthetic Uniformity in Key Metrics   
How it affects analysis: Billing amounts and length of stay show almost zero variance across conditions (e.g., Cancer vs. Obesity billing are nearly identical). This makes real-world clinical pricing inferences unreliable.   
How handled: Focused the project on data engineering workflows, operational frameworks, and capacity metrics rather than drawing absolute clinical pricing conclusions.   
3. Text Formatting & Duplicates   
How it affects analysis: Inconsistent name casing and 534 exact duplicate rows inflate overall admission counts and mess up categorical groupings.   
How handled: Dropped exact duplicates and standardized all string columns to Title Case in Pandas.


Limitations & Unsafe Conclusion
Limitation 1: No hospital operating cost or margin data (we only have billed charges, not profit margins).   
Limitation 2: Missing clinical procedure codes (CPT/ICD) to control for medical acuity or treatment complexity.   
Unsafe Conclusion: Claiming that treating Cancer costs a hospital the exact same amount in real-world clinical practice as treating Obesity or Arthritis.