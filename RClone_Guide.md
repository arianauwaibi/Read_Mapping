# RClone 

## Install RClone on to the Pod 

1. To install rclone on Linux/macOS/BSD systems, run:
```
sudo -v ; curl https://rclone.org/install.sh | sudo bash
```

2. Check install with
```
rclone config
```
create a new remote called ceph

*no region and no location constraints*
  
## Uploading Data to RClone 

```
./rclone copy /Users/arianauwaibi/2018_sequences/Sample_134809_R1_trim.fastq.gz   
```
*The ./ is there because it is needed when using my iMac. Otherwise leave out the ./*

The path from the host computer (iMac) copied to the rclone remote

## Upload Data from RClone to Nautilus Pod
```
rclone copy ceph:sequences /home/jovyan/sequences
```
`/home/jovyan/` is the Nautilus pod home directory
