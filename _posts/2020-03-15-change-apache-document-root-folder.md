---
layout: post
title: How to change the Apache document root folder on a Chromebook
category: chromebook
tags: [linux, apache]
---
# How to change the Apache document root folder on a Chromebook

1. Open Terminal
2. Run `cd` to make sure you're in your home directory:
3. Copy the `000-default.conf` file to your home directory:
`cp /etc/apache2/sites-available/000-default.conf ./`
4. Open the `000-default.conf` in your Chromebook text editor.
5. Edit the `DocumentRoot` option:
`DocumentRoot /path/to/home/directory/www/html`
6. Move `000-default.conf` back to :
`sudo cp 000-default.conf /etc/apache2/sites-available/`

7. Similarly, enable files and directory listing:
`/etc/apache2/apache2.conf`
8. Change `<Directory /var/www/>` to `<Directory /path/to/home/directory/www/>`
9. Then restart the apache server:
`sudo service apache2 restart`



Sources

- https://askubuntu.com/questions/337874/change-apache-document-root-folder-to-secondary-hard-drive
- https://francescoficarola.com/apache-enable-files-directory-listing/
