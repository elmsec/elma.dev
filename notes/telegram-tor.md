---
title: "Running Telegram via Tor on Linux"
date: 2020-11-08T16:57:21+03:00
draft: false
description: "You can circumvent internet censorship and unblock Telegram with Tor."
toc: false
---

If you are in a country that cencors Telegram or if you are connecting from a private network that requires a proxy, you can use Tor to run Telegram.

## Install the Tor package
Use the commands below to install the `tor` package on your computer.  

__on Arch Linux:__
```bash
sudo pacman -S tor
```
__on Ubuntu:__
```bash
sudo apt-get install tor
```

## Start the Tor service
After installing the `tor` package, you should start the `tor.service`:
```bash
sudo systemctl start tor.service
```

This will start the tor service and you will be able to use it on port 9050.

## Add your custom proxy to Telegram
Open the Telegram Desktop app and go to the __Settings > Advanced > Connection type__. Check the box that says __"Try connecting through IPv6"__. Also click on the __"Use custom proxy"__ selection.

Now you can add a Tor proxy. Click the __ADD PROXY__ button. __SOCKS5__ should be selected in the opened window. In the __Socket address__ section, set the __Hostname__ to `127.0.0.1` and the __Port__ to `9050`.

That's all. Click the __Save__ and Telegram will try to connect via this proxy.

To make this step faster, you can use this link as an alternative:  
[https://t.me/socks?server=127.0.0.1&port=9050](https://t.me/socks?server=127.0.0.1&port=9050)



> **Note:** Tor by itself is not all you need to maintain your anonymity. There are several major pitfalls to watch out for _(see: [Want Tor To Really Work?](https://en.calameo.com/read/005242387ef11d44d4ae7))_.
