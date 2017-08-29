---
layout: post
title:  "Installing Node.js on a Raspberry Pi 3"
date:   2016-11-02 20:55:00 +0100
categories: raspberry linux nodejs raspbian
---
Recently I bought a new Raspberry Pi 3 and wanted to run a few Node.js applications on it. Unfortunately the Node.js version that is available on [Raspbian](https://www.raspbian.org/) is quite old.

Don't worry, it's easy to install. Follow the instructions below and you're all set.

```bash
$ sudo apt-get update
$ curl -sL https://deb.nodesource.com/setup_7.x | sudo bash -
$ apt-get install nodejs
```

Verify the installation with `node -v`. It should output something like *v7.0.0*
