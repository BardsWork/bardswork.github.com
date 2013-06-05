---
layout: post
title: SonicWALL EnhancedOS Port Forwarding
category: posts
---

SonicWALL is an entry level router that is currently sold by Dell, who purchased the company in 2012. The hardware is well made and comes with an accessible
price tag for anyone looking for some control over their network while not spending a month's rent on a device. They are not cheap, however, entry models 
start at around $200 and they can go all the way up to several thousand dollars for the professional series.

In a small business, the TZ series is an attractive choice based on its price and features. If you are not looking to have over a dozen users on your network
the entry level TZ-100 will suffice, while a larger audience might require a TZ-215. Depending on who you speak with, their opinion will change on which device 
is right for you, however, I believe the "12 Client" rule is good as any to base your decision on.

So now that we went over the introduction lets get on with the Port Forwarding:

To Port Forward in this device, with Enhanced OS, you have two different options. If you are making basic port forwarding, then you can use the wizard on the
upper right hand side of your admin panel - it's fairly straight forward.

On the other hand, if you have to forward unconventional ports, the wizard woun't exactly cut it. There are four steps in the process, so let's get started.

## Step 1
You have to create an Address Object, which is located in your Network settings. Once you are in the panel, click ADD and you will be taken to a preference window.
Here you will specify a name of your Object, the IP address (which is a LAN address), the Type (Host, most likely) and the Zone from which your device is 
operating from.

So far, so good.

## Step 2
Right under Address Object, on the left hand side, click Services. Here you will link Ports with the Address Object and create Service Groups if there are multiple IPs.
First, you should add the Service on the lower portion of the screen. Here you will once again give a Name to your service, select which protocol you will be looking
for to forward (UDP, TCP, etc.) and an IP range for which your ports will need to be forwarded.

Some camera computers might require you to forward TCP as well as UDP ports, in this scenario you will create multiple Services - once the Services have been created
you can then add then to a custome group to make your life easier.

## Step 3
Next, we move to NAT Policies, where you will perform most of your actual routing. Here you might need to create several difference Policies to accomplish your
task. Considering that at times you will need to add Inbound and Outbound policies to comply with your needs, you will have to create each instance individually.

The settings are fairly straight-forward here as you choose the Original and Destination Source, as well as the Translated option. The Original is where your traffic
will be comming from, and the Destination will be where it is going. For Inbound connection, the Translated signal will be WAN Primary IP and for the Destination
you will choose your Address Object that you want to forward to.

Afterwards you will choose the Services that contain the port forwarding information and choose Original as Translated (this will work for most options).

Selecting Interface is as simple as either choosing ANY for both Inbound and Outbound or specifying X1, for example, for WAN, or whatever your configuration is.

It is always a good practice to Comment your work, in the event that you need to remember your work.

## Step 4
Finally we get to the final portion of this brief overview. You will need to go into Firewall and choose the Access Rules panel. Here you will simply choose a Matrix
of where your connection is coming from and where it is going to and then selecing Source, and Destination.

Here you are just allowing all the information to pass through the firewall, and thinking logically through how the signal flows from Origin to Destination, you
will easily pick the right options. 

One example is FROM ZONE: WAN TO ZONE: LAN choosing the WAN IP as Source, Address Object as your Destination and applying the Service you created with the Allow
action selected. This would forward all traffic that is coming in over your ISP and allow it to pass through the network to its Address Object while using
the Service ports.

---

Hopefully this was an easy tutorial to follow, but if you run into any issues, please feel free to Tweet and/or Email me and I will do my best to help.

---

[jekyll]: https://github.com/mojombo/jekyll
[zh]: http://zachholman.com
[left]: https://github.com/holman/left#readme
[twitter]: https://twitter.com/bardworx
