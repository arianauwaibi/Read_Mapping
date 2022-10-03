# Creating a Library for Minimap2 in CoverM

-r, --reference 

*Minimap2 adds extra*
-p minimap2-no-preset

```
-r --minimap2-reference-is-index
```

Include the path of the reference genome 

```
 coverm genome -1 Sample_134807_R1_trim.fastq -2 Sample_134807_R2_trim.fastq --reference strain_BS13-02.fna --minimap2-reference-is-index  -p minimap2-no-preset
 ```

## Format for code

  **coverm**
  
  **genome** 
  
  --contig-end-exclusion <contig-end-exclusion>  Dont need
  
  --dereplication-aligned-fraction <dereplication-aligned-fraction> Dont need
  
  --dereplication-ani <dereplication-ani> Dont need
  
  --dereplication-fragment-length <dereplication-fragment-length> Dont need
  
  --dereplication-precluster-method <dereplication-precluster-method> 
  
  --dereplication-prethreshold-ani <dereplication-prethreshold-ani> 
  
  --dereplication-quality-formula <dereplication-quality-formula> 
  
  --genome-definition <genome-definition>

  **--genome-fasta-directory <genome-fasta-directory>**
  
  **--genome-fasta-extension <genome-fasta-extension>** 
  
  --genome-fasta-files <genome-fasta-files>... 
  
  --genome-fasta-list <genome-fasta-list> 
  
  **--mapper <mapper> --methods <methods>...** 
  
  --min-covered-fraction <min-covered-fraction> 
  
  **--minimap2-reference-is-index**
  
  **--output-format <output-format>**
  
  **--read1 <read1>...**
  
  **--read2 <read2>...**
  
  **--reference <reference>...** 
  
  --separator <separator> 
  
  --threads <threads> 
  
  --trim-max <trim-max> 
  
  --trim-min <trim-min>
  
  
  
  ## Part of the Format I Need So Far
  
  coverm

  genome
  
  --genome-fasta-directory <genome-fasta-directory>
  
  --genome-fasta-files <genome-fasta-files>...
  
  --interleaved <interleaved>...
  
  --read1 <read1>...
  
  --read2 <read2>...
  
  --mapper <mapper> 
  
  --methods relative_abundance
  
  --minimap2-reference-is-index
  
  
  ```
  coverm genome --read1 Sample_134807_R1_trim.fastq --read2 Sample_134807_R2_trim.fastq --minimap2-reference-is-index --genome-fasta-directory Strains/ --genome-fasta-extension .fna --methods relative_abundance 
  ```
  
