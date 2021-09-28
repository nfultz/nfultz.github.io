<!-- njnmdoc:  title="Firefox"  -->
Firefox is the open-source web browser from Mozilla.

It has several extensions I can't live without:

[Tree Style Tab](http://piro.sakura.ne.jp/xul/_treestyletab.html.en) - Adds a vertical tabbar with nesting.

[No Close Buttons](https://addons.mozilla.org/en-US/firefox/addon/no-close-buttons/) - remove the close button from tabs. Used to be in <code>about:config</code>

[Tab History Redux](https://addons.mozilla.org/en-US/firefox/addon/tab-history-redux/) - new tabs inherit history from their parent.

[RightBar](https://addons.mozilla.org/en-US/firefox/addon/rightbar/) - moves sidebar to right

<code>about:config</code> holds all sorts of settings that firefox uses. Like the warning says, changing them will void your warranty.

# Change layout of speeddial

browser.newtabpage.rows

browser.newtabpage.cols

# Disable autoadding www and .com to domains

browser.fix.alternate.enabled

Netflix and Amazon instant video both use Microsoft Silverlight to server videos, which isn't supported on linux. However, you can run Silverlight in WINE to achieve the same result.

[About Pipelight](http://fds-team.de/cms/articles/2013-08/pipelight-using-silverlight-in-linux-browsers.html)

[PPA](https://launchpad.net/~mqchael/+archive/ubuntu/pipelight)

In order to boot X11 straight in to Firefox (or on Debian, Iceweasel) with no window manager, drop the following into /usr/share/xsessions/

[Desktop Entry]

Name=Iceweasel

Comment=Nothing but web

GenericName=Web Browser

Exec=/usr/bin/iceweasel

Type=Application

Icon=iceweasel

Categories=Network;WebBrowser;

StartupWMClass=Iceweasel

StartupNotify=true



<h2>Force enable hardware acceleration</h2>



Note: If hardware acceleration is disabled for a specific hardware, it may be due to stability issues or high system resources consumption. Proceed with force-enabling it at your own risk.<p>



To check if acceleration is enabled, go to about:support and under the "Graphics" section look for "GPU Accelerated Windows". If it reports "0/1 OpenGL (OMTC)" (possibly 0/2), acceleration is disabled; if it reports "1/1 OpenGL (OMTC)" (possibly 1/2 or 2/2) it is enabled.<p>



To enable acceleration go to <code>about:config</code> and set:



<pre><code>

    layers.acceleration.force-enabled true

    layers.offmainthreadcomposition.enabled true

</code></pre>



Finally, export the <code>MOZ_USE_OMTC=1</code> environment variable, for example:





<pre><code>

/etc/profile.d/mozilla-common.sh



export MOZ_USE_OMTC=1

</code></pre>



Restart X server or reboot for the change to take effect.

