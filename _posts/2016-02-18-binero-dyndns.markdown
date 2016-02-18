---
layout: post
title:  "Binero DynDNS"
date:   2016-02-18 07:00:00 +0100
categories: binero dyndns synology
---
I have an old Synology DS213j NAS that I want to use for DynDNS. Now Synology does support DDNS but does not come with my DynDNS provider, [Binero](https://www.binero.se), preconfigured. Follow these easy steps to add support for Binero DynDNS in your Synology NAS

## Prerequsities - Verify that DynDNS is correctly setup.

* Use curl or a browser and call `https://EMAIL:PASSWORD@dyndns.binero.se/nic/update?hostname=HOST&myip=IP` make sure you set EMAIL, PASSWORD, HOST and IP
* You should get a response that says good or similar.

## Add Binero DynDNS to Synology

* Use SSH and log into your NAS.

* Edit `/etc.defaults/ddns_provider.conf` and add the this block at the end of the file

<pre>
[Binero]
  modulepath=DynDNS
  queryurl=dyndns.binero.se/nic/update?hostname=__HOSTNAME__&myip=__MYIP__
</pre>


* Now log into your NAS and open `Control Panel -> External Access` and click on Add in the DDNS tab. Binero should now be in the list of Service Providers

* You're all set up! You should see your service provider and hostname in the list and status should be `Normal`
