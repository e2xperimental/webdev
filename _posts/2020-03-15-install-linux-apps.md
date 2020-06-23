---
layout: post
title: How to install linux apps
date: 2020-03-15
category: chromebook
tags: [linux]
---

# Installing linux apps on a Chromebook

## Run updates

In Terminal, check all the repositories to see if you need any updates.

`sudo apt update`

or `sudo apt-get update`*

Check to see which of your packages are upgradable.

`apt list --upgradable`

Then type this to update them.

``sudo apt upgrade`
...
Do you want to continue? [Y/n]   y``

Install FireFox:

`sudo apt-get install firefox-esr`

Install a photo editor:

`sudo apt-get install gimp`

Install an audio editor:

`sudo apt-get install audacity`

Find a list of all stable debian packages:
https://packages.debian.org/stable/

## Next steps
- What linux apps come with my Chromebook Acer R 13?
- Understanding the Linux Filesystem on your Chromebook
- Install linux software on a Chromebook Acer R 13
- Turn on GPU acceleration on Chromebooks

## Source
- [Ubuntu made easy](https://www.oreilly.com/library/view/ubuntu-made-easy/9781457169564/)

##* https://itsfoss.com/apt-vs-apt-get-difference/
