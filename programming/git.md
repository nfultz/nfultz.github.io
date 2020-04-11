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


## Git for data

https://github.com/koordinates/sno

https://github.com/liquidata-inc/dolt

https://github.com/iterative/dvc

https://opendata.stackexchange.com/questions/748/is-there-a-git-for-data

http://paulfitz.github.io/daff/

http://dat-data.com/

https://git-annex.branchable.com/

https://github.com/terminusdb/terminus-server/tree/dev

## Revert a file to previous version

```
git checkout $(git rev-list -n 1 HEAD -- "$file")^ -- "$file"
```

