# mvvmlight
Git mirror of GalaSoft MVVM Light Toolkit (https://mvvmlight.codeplex.com/)

## Mirror setup
Install hg-git (https://github.com/schacon/hg-git)
```
$ pip install hg-git
```

Enable the extension by modifying `~/.hgrc`
```
[extensions]
hgext.bookmarks =
hggit =
```
You can verify that worked by typing `hg help hggit`

Clone a Git repository
```
$ hg clone https://hg.codeplex.com/mvvmlight
```

Setup pushing an existing Hg repository to Git
```
$ cd mercurial-repo
$ hg bookmark -r default master # so a ref gets created
```
To avoid specifying the repo path when you push and pull, edit `.hg/hgrc` and add (where _github_ is a friendly name):
```
[paths]
github = git+ssh://git@github.com/timdetering/some-repo.git
```

Push to Git repository
```
$ hg push github
```

## Links
- http://stackoverflow.com/questions/2670158/mirroring-a-hg-project-from-bitbucket-to-github
- http://mohundro.com/blog/2013/07/01/converting-a-mercurial-repository-to-git/
- http://hg-git.github.io/
- https://github.com/felipec/git-remote-hg
- http://hgtip.com/tips/advanced/2009-11-09-create-a-git-mirror/
