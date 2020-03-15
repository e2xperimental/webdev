---
layout: post
title: How to run PHP scripts on a Chromebook
date: 2019-12-01 13:00:00 -0000
category: chromebook-linux
tags: [php, how-to-run]
---
# How to run PHP scripts on a Chromebook

1. Start Apache.

`sudo service apache2 start`

If you haven't installed Apache and PHP, read that first.

## Create PHP script

2. Change the current working directory to the location where you want the script(s).

`cd /var/www/html/`

Put your PHP script somewhere in that folder or

[Clone a GitHub repository](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository)

a. On GitHub, navigate to the main page of the repository.

b. Under the repository name, click Clone or download.

c. Copy the URL under "Clone with HTTPS" or "Use SSH"

d. In Terminal, type `git clone`, and then paste the URL you copied in Step c.

`git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY`

f. Press Enter. Your local clone will be created.

g. To refresh your repository:

`git fetch`

[Git cheatsheet](https://help.github.com/en/github/getting-started-with-github/git-cheatsheet)

## Run from Chrome browser

3. Get your IP address
4. Open the Terminal app and type:

`hostname -I`

5. Paste the IP address into Chrome, you should see an Apache2 Debian Default Page.

If the IP address doesn't work, paste `http://penguin.termina.linux.test/` into Chrome.

## Run from command line

`php /var/www/html/phpinfo.php`

## PHPinfo

If you are only interested in the output of phpinfo() you can see the same information from the command line with:

`php -i`

This prints it in a console-friendly format, rather than in styled HTML as phpinfo() displays.

Stop Apache:

`sudo service apache2 stop`
