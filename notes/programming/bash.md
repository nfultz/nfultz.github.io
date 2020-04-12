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













