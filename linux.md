<!-- njnmdoc: title="Linux Notes"  -->


## Mirroring from s3 to ftp

    * Launch ec2 node 
        * in same region as bucket, for free transfer
        * Need not be too large, this will be IO/network bound
    * Mount s3 bucket using s3fs
        * Tricky if there is a dot in the bucket name
        * `s3fs -o -o -o <bucketname> <mountpoint>` #TODO
    * recursive copy using `ncftp`
        * `mput -R .`
