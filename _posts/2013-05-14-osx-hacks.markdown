---
layout: post
title: OSX Hacks
category: posts
---

Are there annoyances in OS X Mountain Lion that bug you to hell? Are you mad that you can’t hold one key to type a line of A's or wish you could have shut off the Notification Center? Well, you’re in luck because today we will list some of the more useful commands in Terminal that can do just that, and so much more.

## Key Repeating

In the new variation of Apple OS X, Mountain Lion, if you hold down a single key, such as “A”, you will not get an unlimited supply of letters to use to your heart’s content, instead you will have an auto correction feature and/or different styles of a letter pop up. This might be useful at times but annoying if you are trying to simply type “yeaaaaaaaaah!”. To re-enable repetitive key presses, you just need to launch Terminal from Applications and type the following command, followed by ENTER.

> `default write -g ApplePressAndHoldEnabled -bool false`

After executing the following command you have to log out of your account and log back in to enjoy the new function. If you ever get tiered of typing unlimited amount of “Os”, you can return the auto-correct feature by typing;

> `default write -g ApplePressAndHoldEnabled -bool true`

## Disable Notification Center & Remove the Menu Bar Icon

For some, Notification Center is a gift while to others, its a curse. If you are in the latter category then the following commands will remove the Notification Center and the corresponding Menu Bar icon - both of these commands remove the features from the current User’s account and has to be replicated under each user if you wish to eradicate the damn tool from your computer.

Open terminal and and type the following command to remove the icon:

> `launchctl unload -w /System/Library/LaunchAgents/com.apple.notificationcenterui.plist`

To kill Notification Center type:

> `killall NotificationCenter`

After freeing yourself from the grasps of Notification Center you might start to miss it or discover that it really was the love of your life, you can return the majestic app by following commands:

> `launchctl load -w /Systems/Library/LaunchAgents/com.apple.notificationcenterui.plist`

Not hit Command + Shift + G and navigate to /Systems/Library/CoreServices/ then find “Notification Center” and double-click the icon to bring back your old friend.

## Rid Yourself of Window Animations

The fine folks at Cupertino have decided that window switching should have animations that instantly induce motion sickness in some people, and if you are one of the unfortunate few who can barely keep their dinner down after 15 minutes of window swapping then I have a fix for you;

In Terminal, type the following;

> `defaults write NSGlobalDomain NSAutomaticWindowsAnimationsEnabled - bool false`

This will not only help keep your food down, it will also make your Mac feel snappier, and both are a good thing. If you start missing the magic that is the swapping animation you can re-enable it using the following command:

> `defaults write NSGlobalDomain NSAutomaticWindowsAnimationsEnabled - bool true`

## Enable AirDrop on Unsupported Macs

AirDrop is incredibly useful when sharing files across files across many computers on the same network. Unfortunately, Mountain Lion is a biased son-ov-a-gun and chooses not to support this holier then holy feature on some of the older Macs.

Typing the following command should help and enable sharing over Ethernet as well:

> `defaults write com.apple.NetworkBrowser BrowserAllInterfaces -tool true`

Remember that this only activates the feature on the current User and you have to re-log to activate.

I hope some of these commands helped you and peaked your interest in the power that is the Terminal app. If you have any questions or would like me to cover something else please don’t hesitate to: Email me, Tweet, or just leave a comment.

Thank for reading!



---

[jekyll]: https://github.com/mojombo/jekyll
[zh]: http://zachholman.com
[left]: https://github.com/holman/left#readme
[twitter]: https://twitter.com/bardworx
