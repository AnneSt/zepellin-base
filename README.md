# zepellin-base
This branch is based on
 * Poky: yocto-2.5.0 (sumo)
 * Kernel 4.14
 * QT: 5.10 (using eglfs)
 * sysvinit

# Zepellin BSP

To get the BSP you need to have repo installed and use it as:

## At first install repo:
```
$ mkdir ~/bin
$ curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
$ chmod a+x ~/bin/repo
```
## Initialize your BSP:

```
$ PATH=${PATH}:~/bin
$ mkdir ~/zepellin-project
$ cd ~/zepellin-project
$ repo init -u https://github.com/AnneSt/zepellin-base.git -b master
$ repo sync -j4
```
At the end of the commands you have every metadata you need to start work with.

## Setup PackagePool:

Create a /opt/packagepool directory and set its permissions:

```
$ sudo mkdir /opt/packagepool
$ sudo chmod 777 /opt/packagepool
```

## Setup Environment

```
$ . setup-environment.sh
```

You will be stand in the build-direcotry. Now you can build your image.

## Build your first Image

```
$ bitbake base-image
```


