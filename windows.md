<!-- njnmdoc: menu="MENU" title="Windows"  -->
## Notes on Windows box

## Broken chrome

Encountered [Issue 838707: Win10 Spring Update 1803 causes ERR_TIMED_OUT](https://bugs.chromium.org/p/chromium/issues/detail?id=838707),

This seems to occur when chrome is installed, and then the spring update is applied, and somehow the system gets into a broken state.
It hoses the system crypto library. Google and MS have both declined to actually fix this.

Actual solution was found in [support forums](https://support.google.com/chrome/forum/AAAAP1KN0B0s5S1uPI0kMc/?hl=en&gpf=%23!msg%2Fchrome%2Fs5S1uPI0kMc%2FPVBgVbx6DAAJ&msgid=PVBgVbx6DAAJ),
but you will have to click the 'load more comments' button many times, until you see a post by LarryLACa dated 12/6/18

> B) CryptSvc Manual Registry fix instructions, preened from Bug 838707:
> The instructions look long, but will probably take longer to read them than to do.
> You need to delete the Root level, but it takes a few steps to get there and be safe along the way.
> The instructions boil down to:
> 1. Open Run, type in regedit
> 2. Go here: HKEY_CURRENT_USER\Software\Microsoft\SystemCertificates\Root\
>
> 3. Right-click ProtectedRoots > Permissions and pick your account .
>
>     Tick Allow Full Control
>
> 4. Open Task Manager > stop Cryptographic Service
> 5. In regedit, delete Root (HKEY_CURRENT_USER\Software\Microsoft\SystemCertificates\)
>
> 6. Restart Windows
>
> For detail instructions, see B.1 below

## Broken clock

Windows defaults to local time instead of UTC; to use UTC,

    [HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\TimeZoneInformation]
    "RealTimeIsUniversal"=dword:00000001
