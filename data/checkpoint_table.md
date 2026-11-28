## Dataset choice

**Main dataset: GSE65682**

Why we chose it: It has the most deaths (114 of 479 patients), so our estimates are the most precise and a small model will not overfit. It also records processing dates, so we can check for batch effects, and Sweeney's models never used it, so it is a fair independent test.

**Not chosen as main: GSE272769**

Why not: It has fewer deaths (60 of 161), the weakest clinical baseline (only age, sex, shock-yes/no parameters) and no batch information. It also has a 30-day outcome like Sweeney's reference model, one sample per patient (no repeat-sample problem), and an ICU setting similar to MARS, so it is a good external check for our model.

**Not chosen as main: GSE185263**

Why not: Its outcome is in-hospital death with no fixed time window, so it is not comparable with a 28- or 30-day endpoint, and its only ICU site (Toronto, 25% died against 12.1% in emergency rooms) is also the sickest group, so site and severity cannot be separated. It is also the only RNA-seq cohort, with fewer deaths (52) than MARS and 4 very low-read samples, and its counts must be rescaled to log2 counts per million and matched by gene to a model built on arrays. Mixing it into model building would blend platform differences with biology, so we keep it out of the main analysis, whereas Sweeney et al. accepted that trade-off to gain size and diversity. We use it only as a separate secondary check, reported on its own, to see whether the finding holds across technology, setting and outcome definition.

**What worries us about the main dataset:** Several clinical variables contain NA values whose meaning is not stated. Our working interpretation, which we could not confirm, is that for many patients the diagnosis was probably not assessed based on clinicians decision. This affects selecting clinical base predictors (only age, sex and diabetes, or adding pneumonia and thrombocytopenia that have lower completeness rate as well). Using only 3 predictors is weak because any gain from gene expression may look larger than it really is. GSE65682 was deposited already normalised and batch-corrected, so we cannot check batch effects ourselves, and processing date is tied to enrolment period, so a date effect cannot be separated from a cohort effect. There is no patient ID, so repeat samples cannot be fully ruled out, and "admission sample" is an inference from the papers, not a directly indicated in the data. The 1,500 genes were chosen by variance across all analysis patients, without using the outcome. It is also a Dutch ICU cohort with a 28-day outcome, so our claim applies only to patients like these.

## Checkpoint table

"Expected" numbers are from the student guide. "Our number" is what we counted
ourselves. If the two differ, we explain in the last column.

### GSE65682 (main dataset)

| Check | Expected | Our number | Match? | If different, what we think happened |
|-------|----------|------------|--------|--------------------------------------|
| Rows in clinical table | 802 | 802 | Yes | |
| Columns in clinical table | 22 | 22 | Yes | |
| Healthy samples | 42 | 42 | Yes | |
| ICU samples without outcome | 281 | 281 | Yes | |
| ICU samples with outcome (in_analysis_set = 1) | 479 | 479 | Yes | |
| Rows removed at the filter step (42 healthy + 281 ICU without outcome) | 323 | 323 | Yes | |
| Deaths among the 479 | 114 | 114 | Yes | |
| Survivors among the 479 | 365 | 365 | Yes | |
| Missing diabetes among the 479 | 89 | 89 | Yes | |
| Rows in expression table | 802 | 802 | Yes | |
| Columns in expression table (GSM + 1,500 genes) | 1,501 | 1,501 | Yes | |
| Rows matched after joining clinical and expression (lost) | 802 (0 lost) | 802 (0 lost) | Yes | |
| Probes in matrix | 24,646 | 24,646 | Yes | |
| Probes with a gene symbol | 24,553 | 24,553 | Yes | |
| Processing dates (batches) | 14 | 14 | Yes | |
| Gold samples among the 479 | 380 | 380 | Yes | |
| Silver samples among the 479 | 88 | 88 | Yes | |
| Bronze samples among the 479 | 11 | 11 | Yes | |

### GSE272769

| Check | Expected | Our number | Match? | If different, what we think happened |
|-------|----------|------------|--------|--------------------------------------|
| Rows (patients) | 161 | 161 | Yes | |
| Deaths | 60 | 60 | Yes | |
| Survivors | 101 | 101 | Yes | |

### GSE185263

| Check | Expected | Our number | Match? | If different, what we think happened |
|-------|----------|------------|--------|--------------------------------------|
| Samples | 392 | 392 | Yes | |
| Analysis patients | 345 | 345 | Yes | |
| Deaths | 52 | 52 | Yes | |
| Survivors | 293 | 293 | Yes | |

## What surprised us

1. [sentence 1]
2. [sentence 2]
3. [sentence 3]