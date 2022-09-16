# Using CoverM

CoverM contig usage: 

Proper syntax

1. Main Command (coverm)
2. Sub Command (contig)
3. file name or path needed for subcommand
4. Any other subcommands needed
5. Reference

#### Input the Pair Ended Reads

**Forward FASTA/Q file**

  `coverm -1 <the path>`

  *The home part of the path does not have be included. Only include the folder the files are in as the path name. `/home/jovyan/` not needed. Command `pwd` can be used in the linux terminal to access the file path.*

**Reverse FASTA/Q file**

  `coverm -2 <the path>`

**Company Example**
  $ coverm contig --coupled read1.fastq.gz read2.fastq.gz --reference assembly.fna

**This code did not give me an error**
```
coverm contig -1 Sample_134807_R1_trim.fastq.gz -2 Sample_134807_R2_trim.fastq.gz --reference reference_strains/strain_BS13-02.fna.gz
```



### The Commands needed for Success

**1. Main command- CoverM**
 
 ```
  coverm
  ```

**2. -1 (forward read)**

```
-1 Sample_134807_R1_trim.fastq.gz
```

**3. -2 (reverse read)**

```
-2 Sample_134807_R2_trim.fastq.gz
```

**4. --reference** 

```
--reference reference_strains/strain_BS13-02.fna.gz
```

**5. --mapper *default: minimap2-sr**

**6. Alignment Thresholding**

**7.  --methods *default: mean**

**8.  --output (file)**
