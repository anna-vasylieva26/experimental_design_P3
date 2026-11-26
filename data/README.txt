P3 data package: sepsis blood transcriptome and outcome. REAL public data from NCBI GEO. Frozen 21 November 2026. Public records; cite the GSE number and its paper.
Three cohorts. Start with GSE65682.

GSE65682 (microarray, ICU patients, 28-day death)
  GSE65682_clinical_802.csv                         one row per SAMPLE (802: 42 healthy, 281 ICU without outcome, 479 ICU with outcome). in_analysis_set = 1 marks the 479.
  GSE65682_expression_top1500_genes.csv             802 rows x 1,500 genes (log2 intensity, normalised and batch-corrected by the authors). Join on GSM.
  GSE65682_selected_genes_top1500.csv               gene symbol, probe id, variance (chosen without the outcome: see the guide, section 5.2).
  GSE65682_probe_to_gene_all_probes_in_matrix.csv   all 24,646 probes with gene symbol, title, Entrez id.
  GSE65682_batch_by_outcome.csv                     processing date (inferred from the sample title) by outcome.
GSE272769 (microarray, ICU sepsis, 30-day death)
  GSE272769_clinical_161.csv, GSE272769_expression_top1500_genes.csv, GSE272769_selected_genes_top1500.csv, GSE272769_probe_to_gene_all_probes_in_matrix.csv
GSE185263 (RNA-seq, emergency room and ICU, in-hospital death)
  GSE185263_clinical_392.csv (392 samples incl. 44 healthy; library size included), GSE185263_raw_counts_top1500_genes.csv,
  GSE185263_log2cpm_top1500_genes.csv, GSE185263_selected_genes_top1500.csv, GSE185263_site_by_outcome.csv

Warnings: columns named DO_NOT_USE_* and SOFA_24h_after_admission_NOT_BASELINE must not be used as predictors.
The expression files hold only the 1,500 most variable genes. Check your copies with MANIFEST_md5.txt.
