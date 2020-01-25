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

## ClamAV from source

  * Get tarball and install:
      * `./configure`
      * `make`
      * `sudo checkinstall` - choose 'don't copy' for files in build and home dir
  * `sudo ldconfig /usr/local/lib`
  * `sudo cp /usr/local/etc/freshclam.conf{.sample,}`
      * Edit
  * make shared folder:
      * `sudo mkdir /usr/local/share/clamav`
      * `sudo chgrp 130 /usr/local/share/clamav`
      * `sudo chmod 776 /usr/local/share/clamav`
  * `sudo freshclam` to update virus defs

## Cisco AnyConnect VPN

  * `sudo apt install network-manager-openconnect-gnome`
  * Start `nm-applet` - this may require the gnome-tweak to show indicators
      * https://bugzilla.redhat.com/show_bug.cgi?id=1394977
  * Better debugging: ```
sudo nmcli general logging level TRACE
journalctl -u NetworkManager --since '2 minutes ago'
```

## FoxyProxy config

  * Add New Proxy
      * host - "localhost"
      * port - 9999
      * Socks Proxy checked, SOCKS v5 selected
      * Add rule *neal-nuc*
  * ssh -D 9999 nfultz@neal.nuc
  * visit http://neal-nuc:8787 from chrome

## Enable Bluetooth at boot

  * From [TomTom](https://unix.stackexchange.com/a/199088/50441):
  * Add to /etc/udev/rules.d/10-local.rules :```
 # Set bluetooth power up
ACTION=="add", KERNEL=="hci0", RUN+="/usr/bin/hciconfig hci0 up"
```
