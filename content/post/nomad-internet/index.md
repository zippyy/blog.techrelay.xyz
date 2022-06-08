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

**1: You must have another GL-Inet Router or a Raspi, Old Desktop, Home router, etc... that supports wireguard(openvpn can be used as well albeit at a slower perfomance)

**2: If your setup does not have wireguard functionality already setup like a turnkey raspi distro, a built in vpn settings in your home router, etc.. then you must setup wg-easy first. (I will Cover This further in this series but for this guide I will assume you bought Two GL-Inet Routers and one will act as the server in your home region while the other goes with you and connects to it.)

**3: You must have a travel router that you will configure to connect to this vpn and take with you on your travels (you can use a home router too that has support for something like openwrt if you plan to be stationary as well)


For this Guide I will be using a GL-Inet Flint (GL-AX1800) as the Home region router refered to as HomeRouter in the rest of this guide and a Slate (GL-AR750S) as the Mobile travel router refered to as TravelRouter in the rest of this guide. 


Alright lets get started. 

Take the HomeRouter and connect it to the internet, If you already have a router for you home internet (like a dsl modem/router combo or an xfinity gateway, either make sure its in bridge mode so that the Home Router is acting as the dhcp server and routing point or if your device does not support bridge mode or you have a nicer router then you will need to port forward to the HomeRouter)

Assuming you have purchased the recomended routers in this guide then you just need to connect a device to the router, open a browser and connect to the web portal, For most GL-Inet routers this will be 192.168.8.1 but you should have a little card that comes with it that has the default ip, username and password documented on it. Once you are logged into the portal go to VPN -> WireGuard Server. Click Initialize WireGuard Server

Screenshot goes here

choose the IP address subnet on the next screen. you can leave this as whatever the default is, on mine it was 10.0.0.1, I changed this to 10.0.42.1 (shout out to HHGTTG) but this can really be anything starting with 10.0.x.x (remember only 1-254)

screenshot goes here 

On that same screen you can set the port that the vpn will connect to. This can be left as the default or if you know that you will be connected to networks with strict outgoing port lockdowns you can set this to something like port 53 (DNS), port 80 (http), port 443 (https) or another common port that is rarely blocked however this is only needed for more complicated setups or if you want to attempt to bypass paid hotspots, I say attempt because it doesnt work for all of them and is becoming less common as most have switched to more advanced ways of detecting, and others are even easier like simply mac spoofing your device but thats a whole other topic in and of itself so I digress lol.


