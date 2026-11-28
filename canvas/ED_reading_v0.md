ED READING v0 - team 3 - Project 3: Gene Expression in Sepsis Mortality Prediction

1. Kind of study: prognostic-model study - building a model on secondary data answering a project question - does blood gene-expression data provide incremental predictive value beyond routine clinical variables in predicting death in sepsis patients.  
2. The units:
(a) the experimental unit - "none" because data is secondary and no treatment is applied to any object in this study;
(b) the observational unit - ICU patients, healthy controls;
(c) the unit of inference - ICU patients with sepsis.
3. n at each level (count, from your data): 
Dataset 1 (GSE65682): 802 total observations; 479 included in analysis ICU patients; 232 with pneumonia or abdominal sepsis.
Dataset 2 (GSE185263): 392 total observations; 345 included in analysis ICU patients with sepsis
Dataset 3 (GSE272769): 161 critically ill sepsis patients (all observations)
Which of these counts does your claim rest on? - 232, 345, 161 ICU sepsis patients from 2 datasets.
4. The five design types. For each write APPLIES / PARTLY / NO and one sentence of reason
that points to something you saw in the data:
- Completely randomised: NO, nothing was randomly assigned, only fact of disease, death and survival observed;
- Randomised block (designed or found?): PARTLY - found block - by enrolment date and site (batch efects)
- Factorial / crossed (are any cells empty?): PARTLY - two predictive models are build (based on clinical variables, and gene-expression) and effects of two models are added 
- Nested: PARTLY - one dataset indicats nesting by hospital (patient may share same characteristics of treatment, etc.), in the main dataset nesting is not defined
- Repeated measures / matched pairs (is it really the same material measured again?): PARTLY - in the main dataset paired measurements for some characteristics (ICU_acquired infections) are present; study design provides comparison of three models on each patient - results are paired for each tested patient. 
5. The most worrying confounding you can see (two things tied together), and the table that shows
it: (1) expression level ted to blood cell relative concentration - in patients with sepsis proportion of neutrofils rises and expression of genes associated with them as well;
(2) sex-chromosome genes are the most varied but confounded with patients sex;
(3) steroid treatment affects gene expression - when administered to sepsis patients create a risk of gene expression confounding (no record of steroids use in clinical data)
(table GSE65682_expression_to
p1500_genes) 
6. One question you want to ask the instructor: Given the differences between GSE65682 and GSE185263, particularly in outcome definitions and data collection, should we combine them into one dataset for model development, or analyse them separately and use one for external validation?