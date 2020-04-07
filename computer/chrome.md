<!-- njnmdoc: title="Chrome Notes"  -->


## Force pdfs to download

> There is a setting for this now (Version 61):
>
> *Go to:* chrome://settings/content
>
> Scroll down to the PDF-documents section and select option to Download PDF files
>
> Not sure exactly when this was changed. In version 58 there is a similar option to Open PDF files in the default viewer, but this has the same effect in linux (possibly different on other platforms).

from https://superuser.com/a/1260507/313253 by jonasfh

## IndexedDB Eviction

IndexedDB is interally stored in LevelDB, and subject to the LRU policy when space is low.

If GoToMeeting goes berserk, fills up the disk and then crashes chrome, every single DB will be gone. :(

## Good Extensions

  - [ublock Origin](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
All around awesome ad blocker.
  - [Great Suspender](https://chrome.google.com/webstore/detail/the-great-suspender/klbibkeccnjlkjkiokjodocebajanakg)
Hibernates unused tabs automatically, freeing up resources for other things.
  - [Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/iodihamcpbpeioajjeobimgagajmlibd)
Highly function SSH client with terminal.
  - [Picture-in-Picture](https://chrome.google.com/webstore/detail/picture-in-picture-extens/hkgfoiooedgoejojocmhlaklaeopbecg)
Why doesn't YouTube just do this?
  - [odinochka](https://chrome.google.com/webstore/detail/odinochka/gdoeiedioceagbkajogciogiopdgpoba)
My tab manager of choice.
  - [FoxyProxy](https://chrome.google.com/webstore/detail/foxyproxy-standard/gcknhkkoolaabfmlnjonogaaifnjlfnp)
Automatically use SSH Tunnels, works with Secure Shell.
  - [Event Merge for gcal](https://chrome.google.com/webstore/detail/event-merge-for-google-ca/idehaflielbgpaokehlhidbjlehlfcep)
Combine duplicate events into a lolipop.
  - [Export History to JSON](https://chrome.google.com/webstore/detail/export-historybookmarks-t/dcoegfodcnjofhjfbhegcgjgapeichlf)
Does one thing well.
  - [Downloads Overwrite Existing Files](https://chrome.google.com/webstore/detail/downloads-overwrite-alrea/lddjgfpjnifpeondafidennlcfagekbp)
No more `file(1)(1)(1)`
  - [Disable HTML5 Autoplay](https://chrome.google.com/webstore/detail/disable-html5-autoplay/efdhoaajjjgckpbkoglidkeendpkolai) i
Can break video-conferencing, but overall a net win.

