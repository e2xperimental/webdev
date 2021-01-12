---
layout: post
title: How to install Node.js
date: 2021-01-11
category: chromebook
tags: [linux]
---

# Installing Node.js on a Chromebook

Node.js is a cross-platform JavaScript runtime environment that allows developers to build server-side and network applications with JavaScript.

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

## Install Node.js:

`sudo apt-get install node`

To see what version of Node you have:

`node -v
v10.23.1`

## NPM

`npm` is bundled with Node.js. It runs on the command line as the command `npm`. It is a package manager that downloads packages into a `node_modules` folder.

You call the downloaded packages through `const libraryModule = require("libraryname")`.

Find a list of all stable debian packages:
https://packages.debian.org/stable/

## Next steps
- How to install Puppeteer

## Source
- [Node.js](https://developer.mozilla.org/en-US/docs/Glossary/Node.js)
