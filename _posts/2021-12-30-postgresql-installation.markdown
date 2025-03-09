---
layout: post
title: "PostgreSQL installation"
comments: true
post_number: 7
date: 2021-12-30 00:00:00 +0100
categories: general
tags: macos postgresql pgadmin installation
---

Hi all,

Today I will describe the installation process of the ``PostgreSQL`` database on the ``macOS High Sierra``.

Some of you may ask: why I describe something like that when today we have technology like containerization,
which solves for us each step and we don't need to focus on little technical issues?  

In my opinion, containerization is something great and very useful to quickly deliver working solutions,  
but when we want to learn what happens under the hood we must go installation process step by step on bare metal.  

I got started at the main web page of [``PostgreSQL``](https://www.postgresql.org).

I found there information about the available **Homebrew** package.

*Hint: How to install **Homebrew** you could find on main web page of the project or use my **[mac-installer](https://github.com/mateusz-piotrowski/mac-installer)** project.*

When we already have **Homebrew** installed we could start the **PostgreSQL** database installation:  

```bash
$ brew install postgresql@<version_number>
```

To handle database state useful will be **Homebrew services**:  
To Install it I only need run the following command:  

```bash
$ brew services
```

Start **postgresql** database:  

```bash
$ brew services run postgresql@<version_number>
```

Check available users:

```bash
$ psql postgres
```

To be able to manage our fresh database useful will be **pgAdmin** application.  
The latest is version 4.  
I install it using the following command:  

```bash
$ brew install --cask pgadmin4
```

When I know available users I can try to connect to the database via **pgAdmin** app.  

It is everything that I have for today.  
Everyone is a blacksmith of own fate.  
Mateusz.

