---
comments: true
date: 2012-12-20 20:00:00
published: true
layout: post
slug: howto-os-x-screenshots-without-shadows
title: "HowTo: OS X screenshots without shadows"
---

The beautiful shadows that OS X brings to screenshots are good in some ways or depending the purpose of the screenshot itself. But for other things are a pain in the ass.

After some research I've found multiple ways to get rid of that shadows

## 1) The default setting
Since the terminal command allows you to deactivate the shadow I assumed that there could be some `defaults` option for the same purpose. And it is!

With this two commands you can use the normal keybinds to do *shadowless* screenshots:
```
defaults write com.apple.screencapture disable-shadow -bool true
killall SystemUIServer
```

To revert to the original status:
```
defaults write com.apple.screencapture disable-shadow -bool false
killall SystemUIServer
```

## 2) The Grab utility

Open the Grab.app: `Applications > Utilities > Grab`, and under the `Capture` menu you will find the `Window` option.

You can also use the `SHIFT`+`CMD`+`W` keybind -while Grab.app is focused-.

## 3) The terminal way

OS X provides us with the `screencapture` command, so we can hack around and build our own scripts. A simple one that allows interactive capture without shadow:

```
screencapture -i -o filename.png
```

A more complete one that saves the screenshot on the desktop with the datetime as filename:
```
screencapture -i -o ~/Desktop/screenshot_`date +%Y%m%d_%H%M%S`.png
```


These are some ways I found. You can play around and make your own bash or Automator scripts and improve it to your needs.

Hope this helps!

