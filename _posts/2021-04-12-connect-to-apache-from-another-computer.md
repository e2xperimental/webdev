---
layout: post
title: How to connect to my Chromebook's Apache server from another computer?
category: "chromebook + apache web server"
tags: [linux, apache]
---
# How to connect to my Chromebook's Apache server from another computer?

## Get your Chromebook's IP address

1. In Settings, go to Linux development environment (Beta) > Port forwarding
2. 
3. 
4. Google, "what is my ip address"
'70.113.50.4
Your public IP address`


2. Open Terminal
Run `hostname -I`
100.115.92.205
3. Run `cd` to make sure you're in your home directory.

## Set the IP address where you'll receive the Apache requests

Do this using the `NameVirtualHost` directive within the apache configuration i.e. httpd.conf/apache2.conf file.

4. Copy the `000-default.conf` file to your home directory:
`cp /etc/apache2/sites-available/000-default.conf ./`
5. Open the `000-default.conf` in your text editor.
6. Edit `<VirtualHost *:80>` to `<VirtualHost *:8080>`
7. Move `000-default.conf` back to :
`sudo cp 000-default.conf /etc/apache2/sites-available/000-default.conf`

6. Copy the `ports.conf` file to your home directory:
`cp /etc/apache2/ports.conf ./`
7. Move `ports.conf` back to :
`sudo cp ports.conf /etc/apache2/ports.conf`

7. Similarly, enable files and directory listing:
`/etc/apache2/apache2.conf`
8. Change `<Directory /var/www/>` to `<Directory /path/to/home/directory/www/>`

## Restart the server

9. Then restart the apache server:
`sudo service apache2 restart`



Sources

- https://support.google.com/chromebook/thread/106121945?hl=en&msgid=106207522#
- https://chromeos.dev/en/web-environment/port-forwarding
- https://www.thegeekdiary.com/beginners-guide-to-apache-http-server/
- https://www.thegeekdiary.com/apache-http-server-most-commonly-used-configuration-directives/
- https://www.guru99.com/apache.html
