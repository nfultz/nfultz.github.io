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

## Fix crackling audio on HDMI

  * From [Gav](https://askubuntu.com/questions/405071/static-and-crackling-in-my-hdmi-audio):
  * Edit /etc/pulse/default.pa :```
# add tsched=0 to udev-detect
load-module module-udev-detect tsched=0
```
  * Other people indicate this might affect ATI specifically.

## Awesome CLI tools

  * epr
    - An epub reader.
    - `pip3 install --user git+https://github.com/wustho/epr.git`
  * ranger
    - An file browser for the terminal
    - `pip3 install --user ranger-fm`
  * pdfbook
    - convert a pdf into a booklet for (double-sided) printing
    - `apt install texlive-extra-utils`
  * [savepagenow](https://github.com/pastpages/savepagenow)
    - saves url to wayback machine
    - `pip3 install --user savepagenow`
  * [youtube-dl](https://github.com/ytdl-org/youtube-dl)
    - scrapes video from youtube
    - `pip3 install --user youtube-dl`
  * [ledger](https://plaintextaccounting.org/)
    - plain text double-entry accouting
    - `apt install ledger`
  * [horcrux](https://github.com/jesseduffield/horcrux)

## Openvpn

```
sudo apt install network-manager-openvpn network-manager-openvpn-gnome
```

Need to reboot!

## Grepping for user cron

```
journalctl | grep --line-buffered -Ei "cron\[[0-9]*\]:\s*\($USER\)"
```

use `--line-buffered` to avoid double-buffer delay.

## Conferences

https://kansaslinuxfest.org/


