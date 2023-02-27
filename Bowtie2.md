# Bowtie 2
  An ultrafast and memory-efficient tool for aligning sequencing reads to long reference sequences. 
  Indexes the genome with an FM Index to keep its memory footprint small
  Supports gapped, local, and paired-end alignment moodes 
  
  ### Build a reference genome index 
  
  ```
  bowtie2-build Microcystis_aeruginosa_PCC_7806SL.fasta test
```
Test refers to the output files name. All the output files will be named **test**

Download the reference genome from NCBI in the **.fasta** format
The **Output** is 6 files

Example:
test.3.bt2.tmp to test.3.bt2
test.4.bt2.tmp to test.4.bt2
test.1.bt2.tmp to test.1.bt2
test.2.bt2.tmp to test.2.bt2
test.rev.1.bt2.tmp to test.rev.1.bt2
test.rev.2.bt2.tmp to test.rev.2.bt2

### Set the parameters for aligning sample reads

Example: 

bowtie2 **--very-fast-local** **-x** /Users/arianauwaibi/bowtie2_index/test **-1** /Users/arianauwaibi/bowtie2_index/Sample_134807_R1_trim.fastq **-2** /Users/arianauwaibi/bowtie2_index/Sample_134807_R2_trim.fastq **-S** /Users/arianauwaibi/bowtie2_index/test.sam

**Parts of the code**
1. End to End alignment or Local Alignment * *default setting* *
-End to End:  searches for alignments involving all of the read characters
-Local: some of the characters at the ends of the read do not participate. In this case, 4 characters are omitted (or "soft trimmed" or "soft clipped") from the beginning and 3 characters are omitted from the end. This sort of alignment can be produced by Bowtie 2 only in local mode.


** End to End Alignment**

## Alignment Score
An alignment score quantifies how similar the read sequence is to the reference sequence aligned to. The higher the score, the more similar they are. A score is calculated by subtracting penalties for each difference (mismatch, gap, etc.) and, in local alignment mode, adding bonuses for each match.

The scores can be configured with the 

--ma (match bonus), 

--mp (mismatch penalty)

--np (penalty for having an N in either the read or the reference)

--rdg (affine read gap penalty) 

--rfg (affine reference gap penalty) options.


#### End to End

#### Local
