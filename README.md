# LAB2_project_group_N11
This project is a fundamental part of the Lab2 exam.

## Data Collection
- We first carried out some preliminary research to select positive and negative data according to specific criteria.  
  The queries used for these searches are stored in the files [`query_neg.txt`](query_neg.txt) and [`query_pos.txt`](query_pos.txt).
- The results were then downloaded in **JSON (uncompressed)** format
- For the positive results, we filtered out entries with a signal peptide (SP) value `< 14` or a cleavage site that was not null.  
- The negative set remained unchanged in number. However, we labeled each entry as **"True"** or **"False"** depending on the presence or absence of a transmembrane helix in the first 90 residues. 
- The final results were converted into two output files:  
  - **TSV** – containing relevant information about each entry.  
  - **FASTA** – containing the sequences of the entries.
- For the TSV files, we extracted only **five specific features** for each entry.
---
## Data Preparation 
- We utilized [`positive.tsv`](positive.tsv) and [`negative.tsv`](negative.tsv) 
- Sequences were clustered separately with MMseqs, applying a 30% sequence identity threshold and 40% coverage.
- The number of unique IDs after clustering was **1193** for the positive set and **8934** for the negative set.
- From these clusters, we generated two new TSV files containing only the representative IDs and their associated features in [`non_redundant_pos.tsv`](non_redundant_pos.tsv) and [`non_redundant_neg.tsv`](non_redundant_neg.tsv)
- We divided the datasets in training (80% positives + 80% negatives) and test (20% positives + 20% negatives) sets 
---
