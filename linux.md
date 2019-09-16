<!-- njnmdoc: title="Linux Notes"  -->


## Mirroring from s3 to ftp

  * Launch ec2 node
      * in same region as bucket, for free transfer
      * Need not be too large, this will be IO/network bound
  * Mount s3 bucket using s3fs
      * Tricky if there is a dot in the bucket name, must `use_path_request_style`
      * If not in us-east-1, most override region
      * Set umask or only root will have permissions
      * `s3fs -o use_path_request_style -o iam_role -o url=https://s3-us-west-2.amazonaws.com -o umask=022 -o endpoint=us-west-2 <bucketname> <mountpoint>`
  * recursive copy using `ncftp`
      * `mput -R .`

## USB HDMI capture

  * `sudo apt install guvcview`
  * `guvcview` to start video capture
  * For audio, there seems to be quite a bit of lag when muxing with video. Instead, open the two streams independently.
    * Find source in `pactl list sources | grep name`
    * Open pulse audio stream in VLC: `vlc pulse://alsa_input.usb-VXIS_Inc_FHD_Capture-02.iec958-stereo`
