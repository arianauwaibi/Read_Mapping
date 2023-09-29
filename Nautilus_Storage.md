# Ceph S3 Storage with Nautilus

## Accessing S3 to upload data

**Download RClone**
1. Downlaod [Rclone](https://rclone.org/downloads/) onto your local computer and the remote 

   - My computer is a Macbook so I use the Intel/AMD-64 Bit option
   - On the remote you can use the command line code
     
      `sudo -v ; curl https://rclone.org/install.sh | sudo bash`
     - ensure RClone is install correctly `rclone -h`

2. Create a remote/ config file
   * If install correctly then continue to create config file
   * `rclone config`
   *  create a new remote
       - Example File
         ```
         ceph:
         type = s3
         provider = Ceph
         access_key_id = ** (provided through Nautilus matrix)
         secret_access_key = ** (provided through Nautilus matrix)
         endpoint = https://s3-east.nrp-nautilus.io
         acl = public-read
         ```
3. Upload your data (time will vary depending on size of file)
    * `rclone copy`

## Mount the S3 volume to your kubernetes pod
