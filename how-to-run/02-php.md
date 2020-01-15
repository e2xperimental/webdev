# How to run PHP scripts on a Chromebook

1. Start Apache.

`sudo service apache2 start`

If you haven't installed Apache and PHP, read that first.

## Download PHP script

2. Put the file somewhere in /var/www/html/

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
