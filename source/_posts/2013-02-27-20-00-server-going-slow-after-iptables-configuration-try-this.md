---
comments: true
date: 2013-02-27 20:45:00
layout: post
slug: server-going-slow-after-iptables-configuration-try-this
title: "Server going slow after IPTables configuration? Try this"
categories:
- system
tags:
- iptables
- linux
---

Recently I've started the migration of my company's servers to a new provider. After checking that the OS installed on the -now- old servers was Ubuntu 8.04 (holy shit), I decided to make a fresh install of CentOS 6.3, cleaning up all the servers contents and setting up everything from scratch.

After setting my iptables rules (INPUT whitelisted, OUTPUT accept all) I noticed a big delay on every connection made to my server. After checking a lot of things, these two solved the issue:

## Enable unilimited traffic on your loopback interface

``` bash
iptables -A INPUT -i lo  -j ACCEPT
iptables -A OUTPUT -o lo -j ACCEPT
```

## Enable traffic for connections started by your server

```
iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT
```

Hope this helps!
