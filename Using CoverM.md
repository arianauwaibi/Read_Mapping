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

```
--minimapper2-
```

**6. Alignment Thresholding**

**7. --methods *default: mean**

**8.  --output (file)**

## Samples


coverm 

contig 

--contig-end-exclusion <contig-end-exclusion> 
  
--mapper <mapper>
  
--methods <methods>...
  
--min-covered-fraction <min-covered-fraction> 
  
--output-format <output-format> 
  
  -1 <read1>...
  
  -2 <read2>... 
  
--reference <reference>... 
  
    --minimap2-reference-is-index 
  
--threads <threads> 
  
--trim-max <trim-max>
  
--trim-min <trim-min>  

  

--minimap2-reference-is-index  
  

  
  **Example**
  
  coverm contig --contig-end-exclusion <contig-end-exclusion> --coupled <coupled>... --interleaved <interleaved>... --mapper <mapper> --methods <methods>... --min-covered-fraction <min-covered-fraction> --min-read-aligned-percent-pair <min-read-aligned-percent-pair> --minimap2-reference-is-index --output-file <output-file> --output-format <output-format> --proper-pairs-only -1 <read1>... -2 <read2>... --reference <reference>... --single <single>... --threads <threads> --trim-max <trim-max> --trim-min <trim-min>
  
**Test 1**
```
coverm contig -c read1.fastq read2.fastq -r BS13-02.fna --minimap2-reference-is-index --mapper --methods --min-read-aligned-percent-pair 95 --output-file results --output-format --proper-pairs-only
```
  
The results of this code did not provide error but it did cause  
 - Warning: coverm Minimap2 uses mapping parameters defined when the index was created, not parameters defined when mapping. Proceeding on the assumption that you passed the correct parameters when creating the minimap2 index.
  
When you wait for 10 mins results popup. Only one read was actually mapped. 
  
  
**Question**
  
 HOW TO CREATE A MINIMAP2 INDEX??
 
  an attempt at creating a index
  
```
coverm contig -1 read1.fastq -2 read2.fastq -r strains.mmi --minimap2-reference-is-index --mapper --methods --min-read-aligned-percent-pair 95 --output-file results --output-format --proper-pairs-only
```
*Results from this code* : Reoccuring error message
  
 [2022-10-12T21:55:48Z WARN  coverm::filter] Found a mapping record marked as being a proper pair, but mtid != tid, indicating it was an improper pair. Record was Record(tid: 236, pos: 39)
 
**Test 2**
  
How to show the length of the contig in the sample
  
```
  coverm contig --single BS13-02.fna -r BS13-02.fna --methods length --output-file lengths_read1_BS13-02.fna_strain
 ```
This provided a chart of the number of scaffolds in the file and the length (bp) of each scaffolds 
  
*Contig	BS13-02.fna/BS13-02.fna Length*
  
*JAADAE010000001.1 -> 85323*
  
coverm contig --single read1.fastq -r read1.fastq --methods length --output-file lengths_read1
