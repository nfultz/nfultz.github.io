<!-- njnmdoc: title="Bash Notes"  -->
## Run in really clean environment

https://unix.stackexchange.com/questions/48994/how-to-run-a-program-in-a-clean-environment-in-bash

```
$ env -i bash --noprofile --norc
```

## Manual

https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html

## Grep notes

* `grep -F`    :: fixed string
* `grep -v`    :: invert pattern
* `grep -q`    :: disable output and early exit.


This note that `grep -vq` succeeds when the file has a non-matching line. I almost always
instead want `!grep -q` which succeeds when there is no matching line. De Morgans Law
is a hell of a drug.

---

According to <i>man bash</i>, there are a couple files in /etc that also get
invoked automatically, so rather than cluttering up everyones home folder with
dotfiles, you can put it there. Neato.

A major vulnerability in bash got exposed Sep 2014 that affected lots of websites.


```
-x

  Echo's the commands to stdout
```

[Handy Bash feature: Process Substitution — Medium](https://medium.com/@joewalnes/handy-bash-feature-process-substitution-8eb6dce68133)

[Cleaning up bash customizations – General Eclectic](http://meta.ath0.com/2007/10/23/cleaning-up-bash-customizations/)












