+++
author = "Nicholas Bennett"
date = 2022-06-08T02:58:03Z
description = ""
draft = false
slug = "nomad-internet"
title = "Digital Nomad Internet Setup"
series = "Digital Nomad"
+++


test draft

Alright so I was browsing Reddit and came across a post in the digital nomad sub asking about covering up your location when working abroad and thus I was compelled to do this write up and actually ended up deciding to do a whole series on DNing, Starting with how to setup your travel router, vpn, kill switch, etc... 

So lets get started. 

First of all lets discuss some pre-reqs that you must have or setup before you start this guide 

**1: You must have a Raspi, Old Desktop, Home router, etc... that supports wireguard(openvpn can be used as well albeit at a slower perfomance)

**2: If your setup does not have wireguard functionality already setup like a turnkey raspi distro, a built in vpn settings in your home router, etc.. then you must setup wg-easy first. I will post a link to a good guide for that part.

**3: You must have a travel router that you will configure to connect to this vpn and take with you on your travels (you can use a home router too that has support for something like openwrt if you plan to be stationary as well)

I will not be covering how to setup wireguard because there are a million good guides out there, I will simply link to a couple good guides for the above pre-req part and strictly cover the travel side of this setup. 

