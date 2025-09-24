# Data preparation

1. Moving the local files containing positive ([```positive.tsv```](https://github.com/Amedeoxa/LAB2_project_group_N11/blob/main/data_collection/positive.tsv)) and negative ([```negative.tsv```](https://github.com/Amedeoxa/LAB2_project_group_N11/blob/main/data_collection/negative.tsv)) datasets to the assigned virtual machine and viceversa with the commands:
   
   ```scp <key_config_alias> <source path> um21@m21.lsb.biocomp.unibo.it:<destination path>```
   
   ```scp -i <key_config_alias> um21@m21.lsb.biocomp.unibo.it:<source path> <destination path>```
3. Clustering the data with the commands:

    ```mmseqs easy-cluster positive.fasta cluster-results tmp --min-seq-id 0.3 -c 0.4 --cov-mode 0 --cluster-mode```

   ```mmseqs easy-cluster negative.fasta cluster-results-neg tmp --min-seq-id 0.3 -c 0.4 --cov-mode 0 --cluster-mode```

4. 

## Results summary

|               | Training set | Test set |
|---------------|--------------|----------|
| Positive      | 874          | 219      |
| Negative      | 7147         | 1787     |
| **Total**     | 8021         | 2006     |
