<!-- njnmdoc: title="Git Notes"  -->
Git is a [[Version Control System]] written by Linus Torvalds.

It is free and open source. It definitely has some warts.

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

## Commonly used git commands:


```
git commit

git pull

git branch

git checkout

git init
```


[Gitorious](http://www.getgitorious.com/) is an open source web thingy for hosting git repos.

It's web admin page is located at <i>http://host/admin</i>, but sometimes it just doesn't work.

 There's also a ruby admin console in <i>/srv/gitorious/app/bin/console</i> that givess more direct access.

[can I make git ignore future revisions to a file? - Stack Overflow](http://stackoverflow.com/questions/4348590/how-can-i-make-git-ignore-future-revisions-to-a-fileHow) <br/> What you are searching for is <br/><code>git update-index --assume-unchanged default_values.txt</code>.

[Gogs, an alternative to Gitlab](http://www.apertoire.net/gogs-an-alternative-to-gitlab/)

[Git from the inside out](https://codewords.recurse.com/issues/two/git-from-the-inside-out)

[GitUp](http://gitup.co/)

[Git Flow considered harmful](http://endoflineblog.com/gitflow-considered-harmful)

I use git-ftp for my script based projects, mostly PHP. Most of the low-cost
web hosting companies do not provide SSH or git support, but only FTP. ---
[Git-ftp by git-ftp](http://git-ftp.github.io/git-ftp/)

