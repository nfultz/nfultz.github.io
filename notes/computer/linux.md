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

### Old awesome commands

* `pv -qL #`  Plays a pipe at # bps
* `figlet`  Large words
* `boxes`
* `crawl`  Better than nethack
* `mc`  Good ole midnight commander file manager
* `mocp`  Midnight commander for music
* `tidy`
* `markdown`
* `freecell`  http://www.linusakesson.net/software/freecell.php
* `colorout`  http://nojhan.github.io/colout/


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


## Old Crunchbang notes



CrunchBang, at [crunchbang.org](http://crunchbang.org) was a [[Debian]]-based [[Linux]] distribution.

It is built with low overhead in mind, making it ideal for modest PCs such as [[netbooks]].

At it's core, it is really just a debian install with good defaults for

[[OpenBox]] - window manager

[[tint2]] - panel

[[conky]] - system info dashboard - Crunchbang lists the OB shortcuts

[A eulogy to CrunchBang, the Linux distro that time passed by | PCWorld](http://www.pcworld.com/article/2882630/the-death-of-a-linux-distro.html#tk.nl_today)


###Creating USB
Default "Create startup USB" in ubuntu did not worked,
installed unetbin, which did.

Set up on laptop. Flash and wireless worked out of box.

### Iceweasel
* Set up quicksearches, changed homepage to ddg,
* get delicious bookmarklet
* Get extensions:
  * RightBar
  * Scrollbar Anywhere
  * TreeStyle Tab
  * Tab History Redux
 in about:config set browser.tabs.loadDivertedInBackground to false.
* Elite proxy switcher is decent too for SOCKS 5 proxy over ssh.


### SSD Notes

Since using an ssd, I did not install a swap partition.

* Therefore, remove the swap line from .conkyrc

### Wlan tweak

Added wlan0 status to conkyrc:

     ESSID: $alignr ${wireless_essid wlan0} ${wireless_link_qual_perc wlan0}%



### Wallpaper Hack

`~/bin/rotate2` is a script for switching desktops

```
     #/bin/sh
     DIR=${1:-~/images/wallpapers}
     FILE=$DIR/$(ls -1tr $DIR | head -n 1)
     touch "$FILE"
     nitrogen --set-zoom-fill "$FILE"
```

`nitrogen` is obviously the command which does the desktop

It is invoked by conky:

    ${execi 222 ~/bin/rotate2}

10/28 : Need this line for conky for fixing
background problems.

    own_window_argb_visual yes

Also added battery meter.

#### Minor stuff

* Set panel to autohide:

    edit .config/tint2, set autohide = 1

* Move notify to bottom right.

    gconftool-2 -s /apps/notify-osd/gravity --type=int 3

  then logout and back in.
  from : http://crunchbanglinux.org/forums/topic/15819/how-to-set-up-notifyosd-in-debian-squeeze-stable/




### Notes from Setting up desktop

Setting up SSD was major pain in the ass, BIOS was defaulting
to IDE emulation and the drive was failing inconsistently
eg ldconfig failures (Invalid ELF; missing magic bytes) and
and segfaulting iceweasel, flash, vim, xterm, everything.

Went through several reinstalls to get it working right. Trick
was to switch it to AHCI.


### Fstab editing
  Because I wanted to still use my old hard drive, two
problems came up:

1) mount it automatically to ~/prev-drive

2) have #! use the HDD swap partition instead of the SSD

Both are accomplished by adding the devices to fstab
along with mount points.

  Since the last time I did this, things have changed, now
you refer to drives by UUID, which you can get out
of blkid

### Grub Editing

  Also, GRUB added all the old drives Ubuntu entries
to the the list, there was ~30 of them. To get rid of them
I commented them out from /boot/grub/grub.cfg; and to make
sure they don't come back, I removed execute permission from
/etc/grub.d/30_os_probe

    sudo chmod -x /etc/grub.ed/30_os_probe

There might be a better way to do this. Also, I had to run
the grub update script once with os probing to get settings
for windows, which I then copied into a diff file (40_win)

###Mcabber

This didn't seem to work until installing TLS libraries.


###Latex

To install Lecture Notes in CS Springer style, unzip llncs2e.zip to

/usr/share/texlive/texmf-dist/tex/latex/llncs2e/

and then rebuild the style database:

    $sudo mktexlsr

I installed the uclathes template there similiarly, by git clone-ing it into
the above directory and rebuilding.


###SSH Shared Keys

first, generate the key

    $ ssh-keygen

then, add it to ssh-agent

    $ ssh-add

check that it is there

    $ ssh-add -L

finally, send it on over

    $ ssh-copy-id remote

Make sure that .ssh is chmod 700 and .ssh/id_rsa is chmod 66

Make sure public key auth is turned on in /etc/ssh/sshd_config


### Text Utils

A couple utils I like for text:

  * boxes
  * figlet
  * pv -pipe view

### Stripping shoutcast streams

     git://src.thregr.org/fIcy

 make and then copy to ~/bin

# Old SUSE Notes

Start with server text only install

Follow these:

http://l3net.wordpress.com/2013/04/24/lightweight-opensuse-lxde-desktop-from-scratch/

```
# zypper install xorg-x11 xorg-x11-server
# startx

# zypper install openbox
```

need Mesa-GL, x drivers for ati and evdev, xorg-video-drivers


http://en.opensuse.org/SDB:Administer_with_sudo

```
# zypper in sudo
# visudo
// add line %sudo ALL=(ALL) ALL
# groupadd sudo
# usermod -a -G sudo neal
```

I don't have man pages, wtf

    sudo zypper in --no-recommends man

apparently man reccomends ghostscript, which is not needed right now.

```
zypper ar http://download.opensuse.org/repositories/X11:/lxde/openSUSE_12.3/X11:lxde.repo

zypper in slim

 ? reccommends ImageMagic ??

zypper in yast2-sysconfig yast2-runlevel

edit /etc/logins.def, remove offending LASTLOG_ENAB

in yast2-runlevel, enable xdm


however, changing systemd default runlevel is a bit more involved:

ln -sf /usr/lib/systemd/system/multi-user.target \
   /etc/systemd/system/default.target

zypper in pulseaudio pavucontrol

zypper in MozillaFirefox
zypper in flash-player


zypper in mercurial
zypper in hg-git

http://susestarter.blogspot.com/2011/03/get-yer-subpixel-hinted-fonts.html

htop
mutt abook
newsbeuter
lynx
moc

ranger from rpm

conky

vlc from videolan.org
libdvdcss from community repo

make
stow from rpm

ncurses-devel

yast2-sshd

autoconf automake

dependencies for st:
libX11-devel fontconfig-devel freetype2-devel libXft-devel libXext libXext6 liberation2-fonts


enable ssh : http://en.opensuse.org/SDB:Configure_openSSH#SSHD_.E2.80.93_The_server
 and firewall in yast

patch

screen with caption patch and 256 color patch

install zathura from github manually, + girara and poppler plugin

install libwebkit, compile tabbed and surf

install R from tumbleweed, install colorout

did a dist upgrade to tumbleweed
```


### Make a motd
    hostname | figlet | boxes | sudo tee /etc/motd

### Old Notes


[Revisiting How We Put Together Linux Systems](http://0pointer.net/blog/revisiting-how-we-put-together-linux-systems.html)

[Why do we use the Linux kernel's TCP stack? - Julia Evans](http://jvns.ca/blog/2016/06/30/why-do-we-use-the-linux-kernels-tcp-stack/)

vmtouch - the Virtual Memory Toucher



Portable file system cache diagnostics and control --- [Hoytech](https://hoytech.com/vmtouch/)

Linux devices manager for the Logitech Unifying Receiver. --- [Solaar](http://pwr.github.io/Solaar/)

[How to switch to Compton for beautiful tear free compositing in XFCE: duncanlock.net](http://duncanlock.net/blog/2013/06/07/how-to-switch-to-compton-for-beautiful-tear-free-compositing-in-xfce/)

[How to Boot Linux ISO Images Directly From Your Hard Drive](http://www.howtogeek.com/196933/how-to-boot-linux-iso-images-directly-from-your-hard-drive/)

[smxi sgfxi svmi :: How to Install the Scripts](http://smxi.org/site/install.htm)

IMO Power user = knowledge of differences between consumer distros, desktop
ricing, and exotic scripts for like media control or home automation Sysadmin =
could do the above but more likely just drinks in between deployments/ fires/
paychecks
  --- [How to tell the level of a Linux book? : linux](http://www.reddit.com/r/linux/comments/2x8rsi/how_to_tell_the_level_of_a_linux_book/)

[The Definitive Guide to Linux System Calls](http://blog.packagecloud.io/eng/2016/04/05/the-definitive-guide-to-linux-system-calls/)

### Links

[A broad overview of how modern Linux systems boot](https://utcc.utoronto.ca/~cks/space/blog/linux/LinuxBootOverview?)
