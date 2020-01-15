# How to run PHP scripts on a Chromebook

1. Start Apache.

`sudo service apache2 start`

If you haven't installed Apache and PHP, read that first.

## Download PHP script

Put the file somewhere in /var/www/html/

## Run from command line

`php /var/www/html/phpinfo.php`

## Run Fetch from web server

`curl http://localhost/phpinfo.php`

(this assumes the web server is configured to run PHP scripts)

## PHPinfo

If you are only interested in the output of phpinfo() you can see the same information from the command line with:

`php -i`

This prints it in a console-friendly format, rather than in styled HTML as phpinfo() displays.

Stop Apache:

`sudo service apache2 stop`
