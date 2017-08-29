---
layout: post
title:  "Setting a static ip on your Raspberry Pi"
date:   2017-08-28 20:55:00 +0100
categories: raspberry pi wifi static
---
Setting a static ip on your Raspberry Pi can be tricky, here's what you need to know.

The easiest way to set a static ip is to add the configuration in ```/etc/dhcpcd.conf```. Edit the file in your favorite editor and scroll down to the bottom of the file.

Add the following configuration:

```
interface eth0
static ip_address=192.168.1.10/24
static routers=192.168.1.1
static domain_name_servers=192.168.1.1
```

Make sure the interface and the network configuration matches your requirements.
