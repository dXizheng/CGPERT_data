CGPERT SUPPORTING DATA

Dataset title
CGPERT: Supporting Data for Codon-Level Prediction of Single-Cell Transcriptomic Responses to Gene Perturbation

Associated manuscript
CGPERT: A Codon-Level Sparse Deep Learning Framework for Interpretable Prediction
of Single-Cell Transcriptomic Responses to Gene Perturbation

Creators, in manuscript order
Jiang Qi-Yu; Zhao Yi-Han; Deng Xi-Zheng; Zhu Sheng-Ling; Zeng Hui-Yan.

Scope
This package contains the 28 CSV/XLSX analysis files supplied with the CGPERT
manuscript. It includes evaluation summaries, training histories, codon importance
scores, domain/subdomain annotations, and derived codon-gene impact/correlation
tables. It is a supporting-data release, not the model implementation or a complete
reproduction package. No scientific values were recalculated or corrected.

Files
Data 01: independent Adamson dataset evaluation summary.
Data 02: model/baseline comparison summary.
Data 03: model/seed performance records.
Data 04: training history in stacked model/seed blocks.
Data 05: gene/codon importance records (165,918 data rows).
Data 06-07: domain and subdomain annotations.
Data 08: cell-level codon correlation summary.
Data 09-18: per-gene codon correlation details for ARID1A, MAPK1, COL1A1, NIT1,
            ZNF318, COL2A1, CBL, GLB1L2, CNNM4 and STIL, respectively.
Data 19-20: codon expression correlations and gene/subdomain summaries.
Data 21: MAPK1 codon expression correlations.
Data 22: MAPK1 absolute codon-gene impact matrix.
Data 23: byte-identical alias of Data 22, retained for source completeness.
Data 24: MAPK1 signed codon-gene impact matrix.
Data 25-26: MAPK1 codon impact summaries and ranked impacted genes.
Data 27-28: MAPK1 codon-gene correlation details and summaries.

DATA_CATALOG.csv records file sizes, SHA-256 digests, field names and worksheet
information. CSV row counts exclude the header. XLSX data_rows counts nonempty
rows after the first nonempty row; Data 04 contains additional block labels and
headers, so this count is not a count of training observations. Empty sheets are
retained exactly as supplied.
SHA256SUMS.txt provides checksums for every payload and documentation file,
excluding itself. Verify files after download with a SHA-256-capable utility.

Reading the files
Read CSV with UTF-8/UTF-8-BOM-aware software. XLSX files can be opened in Excel or
with Python openpyxl/pandas. Summary entries such as mean +/- SD may be stored as
text. Several fields contain comma-separated lists within quoted CSV cells.
Data 22-24 each contain 18 codon rows, three identifier columns and 577 gene
columns. Data 27 contains 10,386 codon-gene rows. Gene symbols are preserved
exactly as supplied. Do not combine absolute and signed values interchangeably.
Data 05 uses the field codon_idx; other files use codon_position. Position indexing
must be checked against the originating analysis before joining these fields.

Provenance
The manuscript reports training/evaluation using previously published human K562
Perturb-seq datasets from Norman et al. (2019) and Adamson et al. It also describes
secondary analysis of primary CML patient-cell expression data from GSE206421:
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE206421
These upstream resources remain credited to their original creators. This package
contains the supplied derived analysis exports; it does not redistribute raw GEO
sequence data or claim ownership of upstream datasets.
Norman et al. (2019): https://doi.org/10.1126/science.aax4438

Completeness
The supplied package does not include training/plotting scripts, model checkpoints,
complete preprocessed expression matrices or dedicated numerical exports for all
ablation, permutation, counterfactual and primary-CML validation panels. Accordingly,
this release should not be described as containing all data and code needed to
reproduce every manuscript result. The naming and packaging process does not
resolve scientific or statistical questions about the underlying analyses.

Version and rights
Prepared as version 1.0.0 on 24 October 2026. The original 28 data files are
byte-preserved. The authors selected the Creative Commons Attribution-NonCommercial 4.0
International license (CC BY-NC 4.0) for these supporting data:
https://creativecommons.org/licenses/by-nc/4.0/
Reuse is permitted for noncommercial purposes subject to attribution and the
license terms.
Upstream datasets remain subject to their own terms and attribution requirements.
A DOI and repository URL will be added only after they are actually issued.
