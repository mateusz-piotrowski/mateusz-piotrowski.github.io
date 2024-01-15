--- 
layout: post
title:  "PostgreSQL installation"
date:   2021-12-30 00:00:06 +0100
categories: macos postgresql pgadmin installation
---

Hi all,

Today I will describe the installation process of the ``PostgreSQL`` database on the ``macOS High Sierra``.

Some of you may ask: why I describe something like that when today we have technology like containerization,
which solves for us each step and we don't need to focus on little technical issues?  

In my opinion, containerization is something great and very useful to quickly deliver working solutions,  
but when we want learn what happens under the hood we must go a step or steps lower to installation on bare metal.  

I got started at the main web page of [``PostgreSQL``](https://www.postgresql.org).

I found there information about the available **Homebrew** package.

*Hint: How to install **Homebrew** you could find at main web page of the project or use my **[mac-installer](https://github.com/mateusz-piotrowski/mac-installer)** project.*

When we already have **Homebrew** installed we could start **PostgreSQL** database installation:  

```bash
$ brew install postgresql@12
```

To handle database state useful will be **Homebrew services**:  
To Install it I only need run the following command:  

```bash
$ brew services
```

Start **postgresql** database:  

```bash
$ brew services run postgresql@12
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

