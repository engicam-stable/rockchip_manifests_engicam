# Rockchip Linux SDK

## Get repo

###### You have different ways to get repo on your machine.

Many distros include repo, so you might be able to install from there.
```sh
# Debian/Ubuntu.
$ sudo apt-get install repo

# Gentoo.
$ sudo emerge dev-vcs/repo
```

You can install it manually as well as it's a single script.
```sh
$ mkdir -p ~/.bin
$ PATH="${HOME}/.bin:${PATH}"
$ curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.bin/repo
$ chmod a+rx ~/.bin/repo
```

You can clone it from Rockchip.
```sh
$ mkdir -p ~/repo
$ git clone https://github.com/rockchip-linux/repo ${HOME}/repo
$ PATH="${HOME}/repo:${PATH}"
```

## Get repository access
SDK is composed by repo from Engicam and by repo from Rockchip.
Engicam source code is public on Github, but to download from Rockchip git server you need an account
to access the source code repository provided by Rockchip.

## The PX30 chips

Sync to the lastest release code:

```sh
$ mkdir px30 && cd px30

repo init -u https://github.com/engicam-stable/rockchip_manifests_engicam -b px30 -m px30_linux_release.xml

$ .repo/repo/repo sync
```

## The RK3399 chips

Sync to the lastest release code:

```sh
$ mkdir rk3399 && cd rk3399

repo init -u https://github.com/engicam-stable/rockchip_manifests_engicam -b rk3399 -m rk3399_linux_release.xml

$ .repo/repo/repo sync
```
