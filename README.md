# LAB2_project_group_N11
This project is a fundamental part of the Lab2 exam.

## Data Collection
- We first carried out some preliminary research to select positive and negative data according to specific criteria.  
  The queries used for these searches are stored in the files [`query_neg.txt`](query_neg.txt) and [`query_pos.txt`](query_pos.txt).
- The results were then downloaded in **JSON (uncompressed)** format:  
  **2949** entries for the positive set and **20,615** entries for the negative set.
- For the positive results, we filtered out entries with a signal peptide (SP) value `< 14` or a cleavage site that was not null.  
  After filtering, the positive set was reduced from 2949 to **2932** entries, meaning 17 entries were removed.
- The negative set remained unchanged.
- The final results were converted into two output files:  
  - **TSV** – containing relevant information about each entry.  
  - **FASTA** – containing the sequences of the entries.
- For the TSV files, we extracted only **five specific features** for each entry.
