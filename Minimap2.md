# Code for Contig Mapping

Always start with: 
`coverm`

Using the contig mode: 
`contig`

Read Mapping Parameters: 
`-c / --coupled`

--coupled read1.fastq.gz read2.fastq.gz

```
--coupled Sample_134807_R1_trim.fastq.gz Sample_134807_R2_trim.fastq.gz
```

Reference: 
 `-r / --reference`
 
 Since we are using minimap2 we have to use 
 `--minimap2-reference-is-index`
 
 Also include the path of the reference file
 
 ```
 --reference --minimap2-reference-is-index 
 ```
 
 
