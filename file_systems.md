File Systems
============

In order to read a data set, you need to tell R where it is on your
computer.

Your computer's file system is like an upside-down tree.

The **root** is the beginning: the top of your file system.

The name of the root depends on your operating system and computer:

* `/` on Mac OS X and Linux.
* Usually `C:/` on Windows, but sometimes `D:/`, `E:/`, etc...

Each folder or **directory** beneath the root is a branch of the tree.


## Paths

A **path** is a list of directories that lead to a particular place in a file
system. A path can end at a directory or a file.

In a path, directories are separated by forward slashes `/` rather than commas
and spaces.

For example, the file `dinosaurs.pdf`, in the directory `data,` in the
directory `storage`, in the root directory:
```
/storage/data/dinosaurs.pdf
```

R uses forward slashes in paths regardless of operating system. Outside of R,
Windows uses backslashes rather than forward slashes.

If the last part of a path is a directory, you can add a forward slash without
changing the meaning.

So we can write:
```
/storage/data
```

Or equivalently, we can write:
```
/storage/data/
```

The trailing slash helps to disambiguate paths to directories from paths to
files.


## URLs

Website URLs are a more general kind of path:
```
https://boardgamegeek.com/boardgame/297978/mariposas
```

The URL has three parts:

* `https://` is the access protocol
* `boardgamegeek.com` is the name of the computer
* `/boardgame/297978/mariposas` is the actual path


If the last part of the path is a directory, you can optionally add a forward
slash to the end without changing the meaning:
```
boardgamegeek.com/boardgame/297978/mariposas/
```


## Relative Paths

An **absolute path** is one that starts from the root directory.

But we can also imagine a path starting from somewhere else in the tree.
