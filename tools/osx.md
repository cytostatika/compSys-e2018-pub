# OS X tools -- Roll Your Own Toolchain

## gcc and gdb
As standard OS X is setup for using Clang and has even linked `gcc` to run `clang`. We recommend changing it to gcc. The easiest way is the following:

  * Install Homebrew ([http://brew.sh/](http://brew.sh/)) -- Homebrew is a package manager (similar to apt on Linux) that contain ports of many linux programs. (When you get a new Mac, this should be the first program to install, as it is the most useful.)

  * Install gcc. type

  ```
  brew install gcc
  brew install binutils
  ```

  First time Homebrew will install many needed programs (including compiling them for you system), so it can take a long time.

  * Install gdb

  ```
  brew install gdb
  ```

## Code signing GDB
To use gdb on OS X you need it to be code signed. You can find an explanation of how to do it here:
  * [http://andresabino.com/2015/04/14/codesign-gdb-on-mac-os-x-yosemite-10-10-2/](http://andresabino.com/2015/04/14/codesign-gdb-on-mac-os-x-yosemite-10-10-2/)

If you use Sierra, there is an extra step. Follow this manual:
  * [https://gist.github.com/gravitylow/fb595186ce6068537a6e9da6d8b5b96d](https://gist.github.com/gravitylow/fb595186ce6068537a6e9da6d8b5b96d)

## Mount to VM
You can mount home-drive of the VM on your machine using sshfs and work directly on it with your own editors. For this you need to install sshfs:
 * OS X FUSE ([https://osxfuse.github.io/](https://osxfuse.github.io/)). You connect similar to ssh and can use the attached mount shell script. You unmount the directory again using the `umount` command.</p>
