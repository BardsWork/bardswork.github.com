---
layout: post
title: KISS Searies - Networking 101	
category: posts
---

 
For the first installment of this K.I.S.S. (Keep It Simple Stupid) Tech series, I will focus on the basic concepts of the home network. In the beginning of each article there will be K.I.S.S. Bullets to generalize what will be covered, then Meat & Potatoes of the topic to give an overview of each concept, and, in conclusion, the Brain Scratch section which will expand on the topic for the curious. Let's get started.

How Does Your (Home) Network, work.

The goal of this section is to explain your home network, which will be the foundation for later, and larger, discussions on the Internet as a whole. Our K.I.S.S. Bullets" are:

Cover common terms (i.e. Modem, Router, IP, DHCP, Host).
Explain how a simple home network operates and information is routed from ISP (Internet Service Provider) to your PC, and beyond.
Build understanding for future, larger, Internet conversation.
Meat & Potatoes of Home Networking

Your internet at home starts with your ISP (Internet Service Provider) and a Modem - a Modem is a device that receives a signal from your ISP and then sends this signal to-and-fro. Its main job is to send, and receive, a signals - that's it. Think of a Modem like a telephone, it gets hooked up to a line, that has service, and then you can either receive a telephone call or send a telephone call.

Once the signal passes the modem it still needs to reach your devices, and this is where the Router comes in. A Router is an electronic concierge, or receptionist, which takes signals and directs them to their desired destination. While this is not its only function, it is the basic idea behind your Router.  

Now we have a phone ringing (Modem) and a receptionist (Router) picking up that call, but how does our receptionist know who lives in the building (our network) and what's their address? The service that handles such duties is called DHCP (Dynamic Host Configuration Protocol) - the address book of our network. Its function is to assign an IP (Internet Protocol)  address to each device that is attached to our network to ensure that it can communicate with all other devices. DHCP is usually automatic and negotiated between your router and your computer via preset rules - connect your computer, or Host, to the router and automatically an IP address is assigned.

To round out this discussion, lets touch on what exactly is an IP address and a Host. This topic is a bit ambiguous since there are several different types of IP addresses and Host can change meaning depending on the situation; but lets keep to our K.I.S.S. principal and discuss the basics. Every device on your network has an IP Address, which is assigned by a service discussed in a previous section. In addition, every one of those devices could be referred to as a Host, since every device we discussed is "hosting" the information that is coming in. 

Brain Scratch

We only covered the tip of the iceberg when it comes to our home network and each device, or service, discussed could warrant its own post to discuss the complexities. However, before we wrap this up, I would like to touch on a few points for precision. First, nowadays, our modems are actually routers and are inseparable in definition. To have a true Modem, it should be discussed as a Bridged Modem, which literally take the signal and passes it on without using NAT (Network Address Translation), which translates your IP from your home private network to the public Network (internet). When a computer attempts to go to http://www.lifehacker.com, the private IP of the computer is received by our router, which in turn, translate the signal via NAT to the public IP which we receive from the ISP. This process allows the web servers to know where to send back the information.

In addition, for clarity, a public IP is what our ISP assigns the modem/router, which is either dynamic or static. A dynamic IP, mostly used for home services, changes periodically; a static IP, mostly used for business application, is constant throughout. Static, or usable, IPs are an additional service charge and are not offered by all providers for home use. If you type in "Whats my IP" into your favorite search engine, you will receive your public IP.

A private IP is what your router assigns to each computer through DHCP. In most scenarios it looks like 192.168.1.x, where x is an arbitrary number that is assigned. You can always set a "preferred" IP for your device via TCP/IP settings on your OS or via Router with MAC Address Reservation. Preferred IP is useful, but not necessary, for Network Printers or home servers to make data routing easier. 

These are some of the principals that will be covered in future installations of K.I.S.S. of Home Networking which I hope you enjoy, and find educational.

Image was used from [flikr] via [Creative Commons] (Attribution) - [Source]


Thank for reading.

---

[jekyll]: https://github.com/mojombo/jekyll
[flikr]: http://flikr.com
[Creative Commons]: https://creativecommons.org/licenses/by/4.0/legalcode
[Source]: https://secure.flickr.com/photos/amenagement_numerique/
[twitter]: https://twitter.com/bardworx
