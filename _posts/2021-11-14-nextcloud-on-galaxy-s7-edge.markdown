---
layout: post
title: "Nextcloud on Samsung Galaxy S7 edge"
comments: true
post_number: 6
date: 2021-11-14 00:00:00 +0100
categories: general
tags: nextcloud android samsung-s7-edge userland
---

Hi all,

These days, smartphones are little computers that can be put in the pocket.  
Their performance is increasing year by year.  

I thought about which useful application may I run on it.  
The idea of application to install I found in [Jan C. Borchardt](https://github.com/jancborchardt) GitHub account, in [nextcloud-scripts](https://github.com/jancborchardt/nextcloud-scripts/blob/master/nextcloud-on-android.md) repository.

Today, I will describe how I ran **Nextcloud** on **Samsung Galaxy S7 edge** smartphone using the **Userland** app.  

When started the **Userland** app the first time I must choosed the Linux distro,  
on which I want work and connection method.  
I choosed **Ubuntu** in **18.04** version.  
By default, the **Userland** app uses default **Android** connections.  

I tried to check the IP address using ``ifconfig`` command but the``net-tools`` package has not been installed.  

To be able to establish ssh connection from my MacBook I installed ``openssh`` package.  
To start ssh deamon I run ``sshd`` command.  
I checked current user using ``whoami`` command.  

On MacBook, I ran ``ssh <user>@<ipaddress> ``command, but I was not be able to connect.  
I must add a port to command to establish connection - a little help I found on **GitHub** portal in the following thread:
[CyberpunkArmory thread](https://github.com/CypherpunkArmory/UserLAnd/issues/1450)

I ran the following command to prepare the environment for **Nextcloud**:

```bash
$ sudo apt update
```

```bash
$ sudo apt upgrade
```

I installed ``htop`` to monitor the **Galaxy S7 edge** performance but I met an issue that I still do not solve.  

```bash
$ sudo apt install htop
```

To be able to clone **Nextcloud** repository I need ``git``:  

```bash
$ sudo apt install git
```

Editing files will be easier with powerful editor:  
```bash
$ sudo apt install vim
```

The **Nextcloud** need ``php`` and a few dependencies to start so I installed them:   

```bash
$ sudo apt install php
```

```bash
$ sudo apt install php-fpm
```

```bash
$ sudo apt install sqlite
```

```bash
$ sudo apt install coreutils
```

```bash
$ sudo apt install openssl-tool
```

```bash
$ git clone https://github.com/nextcloud/server.git nextcloud
```

```bash
$ cd nextcloud/ && git submodule update --init
```

After the installation of this packages **Nextcloud** returned a message about incorrect ``php`` version,  
from the repository I installed ``7.2`` version, but the required is ``7.3`` version.  

So I removed the packages which I installed,  
and started again installing all packages in correct versions.  

I edit ``sources.list`` file and add the new repository:  

```bash
deb http://ppa.launchpad.net/ondrej/php/ubuntu bionic main
deb-src http://ppa.launchpad.net/ondrej/php/ubuntu bionic main
```
In the next step I tried update the repositories, but retrieved message with issue about Public GPG key.  

The following command fix this issue:  

```bash
$ apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 4F4EA0AAE5267A6C
```

After successfully repositories update I installed the following packages:  

```bash
$ sudo apt install php7.3-sqlite
```

```bash
$ sudo apt install php7.3-zip
```

```bash
$ sudo apt install php7.3-dom
```

```bash
$ sudo apt install php7.3-mbstring
```

```bash
$ sudo apt install php7.3-gd
```

```bash
$ sudo apt install php7.3-curl
```

After successfully packages installation, I start the **Nextcloud** using the following command:  

```bash
$ php -S 0.0.0.0:8080 -t /home/<user_created_during_userland_setup>/nextcloud/
```
The **Nextcloud** has been started successfully.

It is everything that I have for today.  
Everyone is a blacksmith of own fate.  
Mateusz.

