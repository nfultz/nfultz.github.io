<!-- njnmdoc: title="Git Notes"  -->

See also https://www.smashingmagazine.com/make-life-easier-when-using-git/


## Better diff
https://stackoverflow.com/questions/32365271/whats-the-difference-between-git-diff-patience-and-git-diff-histogram

```
git config --global diff.algorithm histogram
```

## Fast switch branches

```
git checkout -
```

## Sort by commit date

```
# To sort branches by commit date
git branch --sort=-committerdate
```

## One-liner to set mtime to last commit time

```
git ls-files | xargs -I{} git log -1 --date=format:%Y%m%d%H%M.%S --format='touch -t %ad "{}"' "{}" | bash
```
