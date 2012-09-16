---
layout: post
title: "Unhide Library folder in MacOS"
date: 2012-09-15 18:03
comments: true
categories: macos
---

In MacOS, Every user's home directory has a bunch of sub-directories that
are hidden. Though they exist, you cant see them generally with Finder.
Whether a particular folder is visible or not is controlled by an 
extended flag that is set for that directory.

If you simply want to see 'Library' directory (folder) always in the
finder, just execute the following commands (in a terminal windows) and you are done.

```
$ chflags nohidden ~/Library/
```

To hide this folder again, simply  remove the 'no' and execute the command.
```
$ chflags hidden ~/Library/
```

To see the extended flags of file/directories, use the '-O' option to ls
like:

```
$ ls -ldO ~/Library
```
