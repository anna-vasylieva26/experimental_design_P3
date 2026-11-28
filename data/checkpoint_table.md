## Dataset choice

**Main dataset: GSE65682**

Why we chose it: [write in your own words]

**Not chosen as main: GSE272769**

Why not: [write in your own words]

**Not chosen as main: GSE185263**

Why not: [write in your own words]

**What worries us about the main dataset:** [write in your own words]

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