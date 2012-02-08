Starting this repo to keep notes about how I got rsync working on Windows.

My next planned step is to create a fully-automated script which will help anyone to run this on their machine (rather than distributing binaries, which I don't want to do).

### How to get RSync on Windows:

- install cygwin (enable rsync package)
- grab those files from `c:\cygwin\bin`
  - rsync.exe
  - cygwin1.dll
  - cygiconv-2.dll
  - (you can double check the list of required dlls using [dependency walker](http://www.dependencywalker.com))
- uninstall cygwin

### How to use

Here's an example call from a Mac OS X machine:

```
rsync -qrlP --delete local-folder user@windows-server-ip:/cygdrive/c/target-folder --rsync-path=c:/tools/rsync.exe
```