# FOG Operating System (FOS)
This is the operating system environment used for imaging with FOG. This is a linux based operating system with all the scripts and programs required for perform imaging tasks.

# What does this repository do?
Builds FOS inits as well as kernels used by FOG.

# What do we need?
1. You'll need a Debian or Red Hat based operating system.
2. You'll need to install git on your system.
3. You'll need to clone the fos repository.

# How do I get the fos repository?
Pull the fos repository with:

```
git clone https://github.com/fogproject/fos
```

# How to build in Debian?





To build the FOS inits and/or kernels we use the `build.sh` script.


#### Build script options:
The `build.sh` script has usage flags that are used to build the inits/kernels. You can run `build.sh -h` or `build.sh --help` to see all the flags.

```
sudo apt-get update; sudo apt-get install make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
```

debian 11 update sources

```
deb http://deb.debian.org/debian bullseye main
deb-src http://deb.debian.org/debian bullseye main

deb http://deb.debian.org/debian-security/ bullseye-security main
deb-src http://deb.debian.org/debian-security/ bullseye-security main

deb http://deb.debian.org/debian bullseye-updates main
deb-src http://deb.debian.org/debian bullseye-updates main
```
#### NOTES:
1. This repository does not contain FOS or the kernels, it contains all the files needed to build the inits and kernels.
2. `/path/to/fos/repo` is not the real path, this is the path to the cloned repository on the machine you plan to run this on. Typically this would be something like `~/fos`. This path <ins>**will**</ins> need to be changed to build.

---

#### Build Everything
```
/path/to/fos/repo/build.sh -n
```
#### Build all inits only
```
/path/to/fos/repo/build.sh -nf
```
#### Build 64 bit (x64) init
```
/path/to/fos/repo/build.sh -nfa x64
```
#### Build 32 bit (x86) init
```
/path/to/fos/repo/build.sh -nfa x86
```
#### Build ARM 64 bit init
```
/path/to/fos/repo/build.sh -nfa arm64
```
#### Build all kernels only
```
/path/to/fos/repo/build.sh -nk
```
#### Build 64 bit (x64) kernel
```
/path/to/fos/repo/build.sh -nka x64
```
#### Build 32 bit (x86) kernel
```
/path/to/fos/repo/build.sh -nka x86
```
#### Build ARM 64 bit kernel
```
/path/to/fos/repo/build.sh -nka arm64
```
