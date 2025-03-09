---
layout: post
title: "Gitea Setup"
comments: true
post_number: 8
date: 2022-01-02 00:00:00 +0100
categories: general
tags: macos postgresql gitea
---

Hi all,

When I already installed and configured the **PostgreSQL** database I can set up the **Gitea** service.

I got started on the main web page of [**Gitea**](https://gitea.com).

I found there information about the available [**Homebrew**](https://docs.gitea.io/en-us/install-from-package/#macos) package.

*Hint: How to install **Homebrew** you could find on the main web page of the project  
or use my **[mac-installer](https://github.com/mateusz-piotrowski/mac-installer)** project.*

When I already have **Homebrew** installed I could start **Gitea** service installation:

```bash
$ brew install gitea
```

After successfully installation, I run **Gitea** via the following command:

```bash
$ gitea
```

In the next step, I configured **Gitea** using the creator available via the web browser.

It is everything that I have for today.  
Everyone is a blacksmith of own fate.  
Mateusz.

