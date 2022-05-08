<!-- njnmdoc: title="ChromeOS Notes"  -->

## Keyboard Shortcuts

Super-[ / Super-]
: Prev/Next Virtual Desktop

Alt-[ / Alt-] / Alt-Dash / Alt-=
: Tile left/right / minimize / maximize current window

## Forticlient VPN (2022)

  * Install Android app


## Cisco AnyConnect VPN

  * Install from https://chrome.google.com/webstore/detail/cisco-anyconnect/jacdijibdjifphcecdielmekkmfdpgee?hl=es-419

## OpenVPN (2017)

  * Boot into dev mode
  * Switch to a virtual console (Ctrl-Alt-F2)
  * run openvpn client on terminal

## Old Notes

Setting up VPN is currently a pain. It appears the ChromeOS GUI only support a json format config file, but OpenVPN server provides bastardized XML.

Enable developer mode (info from chromium.org) <ul>

<li>  On this device, both the recovery button and the dev-switch have been virtualized. Our partners don't really like physical switches - they cost money, take up space on the motherboard, and require holes in the case.

<li>To invoke Recovery mode, you hold down the ESC and Refresh (F3) keys and poke the Power button.

To enter Dev-mode you first invoke Recovery, and at the Recovery screen press Ctrl-D (there's no prompt - you have to know to do it). It will ask you to confirm, then reboot into dev-mode.

<li>Dev-mode works the same as always: It will show the scary boot screen and you need to press Ctrl-D or wait 30 seconds to continue booting.</ul>

Download client config as client.ovpn

Switch to VT2 by pressing Ctrl-Alt-➜ (aka F2)

Log in as chronos, no password needed

<code>sudo /usr/sbin/openvpn ~/Downloads/client.ovpn</code><br/>

This will ask for your login and password

Switch back to VT1



To use window manger shortcuts in Secure Shell, open options then set 'alt-sends-what' to 'browser-key'.

You can also disable the scrollbar



Crouton Cookbook




 --- [Crouton Cookbook | Tom W Wolf](http://tomwwolf.com/chromebook-14-compedium/chromebook-crouton-cookbook/)

[FrancoisBeaufort/posts/JDVkXALPcNq Google Intern has added support to run Crouton¹ in a Chrome OS Window. Thanks…](https://plus.google.com/)

[Screencasting on Chromebooks - nodes](http://blog.ohheybrian.com/2013/04/screencasting-on-chromebooks/)

[Linux on a chromebook](http://www.pants.nu/~jmcminn/toshiba-2015-chromebook-linux.html)

[Economic Value of Chromebooks](http://static.googleusercontent.com/external_content/untrusted_dlcp/ggg.re/en/us/intl/en/chrome/assets/education/pdf/IDC-WP-Quantifying.the.Economic.Value.of.Chromebooks.for.K-12.Education-082012.pdf)

