---
description: First things to setup on a new computer
---

# 🔧 Setup

## Dns

List current DNS servers

```shell-session
$ networksetup -getdnsservers Wi-Fi
```

Setup [Cloudflare DNS](https://1.1.1.1/dns/) servers

```shell-session
$ networksetup -setdnsservers Wi-Fi 1.1.1.1 1.0.0.1 2606:4700:4700::1111 2606:4700:4700::1001
```

Clear DNS server cache

```shell-session
$ sudo dscacheutil -flushcache; sudo killall -HUP mDNSResponder
```

## Software Update

List all available updates

```shell-session
$ softwareupdate --list 
```

Download and install all updates that are recommended for the system and automatically restart (or shut down) if required to complete installation

```shell-session
$ sudo softwareupdate --install --recommended --restart
```
