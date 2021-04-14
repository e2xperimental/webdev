---
layout: post
title: How to run Apache web server on an Acer Chromebook R 13
category: "chromebook + apache web server"
tags: [linux, apache, how-to-run]
---

# How to run Apache web server on an Acer Chromebook R 13

To start Apache 2, run:

`sudo service apache2 start`

To restart Apache 2, run:

`sudo service apache2 restart`

To stop Apache 2, run:

`sudo service apache2 stop`

To gracefully reload Apache 2, run:

`sudo service apache2 reload`

## What is your iP address?

Run: `/sbin/ifconfig`
Under `eth0` look for the number next to `inet`.

## What active connections or ports is your Chromebook listening on?

Run: `netstat -a | more`

````
Active Internet connections (servers and established)
Proto Recv-Q Send-Q Local Address           Foreign Address         State      
tcp        0      0 0.0.0.0:hostmon         0.0.0.0:*               LISTEN     
tcp        0      0 0.0.0.0:2222            0.0.0.0:*               LISTEN     
tcp        0      0 penguin.lxd:http-alt    0.0.0.0:*               LISTEN     
tcp        0      0 127.0.0.53:domain       0.0.0.0:*               LISTEN     
tcp        0      0 penguin.lxd:2222        100.115.92.25:42563     ESTABLISHED
tcp6       0      0 [::]:hostmon            [::]:*                  LISTEN     
tcp6       0      0 [::]:2222               [::]:*                  LISTEN     
tcp6       0      0 [::]:http               [::]:*                  LISTEN     
udp        0      0 127.0.0.53:domain       0.0.0.0:*                          
udp        0      0 0.0.0.0:bootpc          0.0.0.0:*                          
udp        0      0 0.0.0.0:hostmon         0.0.0.0:*                          
udp6       0      0 [::]:hostmon            [::]:*
````
## To see the port numbers

Run: `netstat -an | more`

````
Active Internet connections (servers and established)
Proto Recv-Q Send-Q Local Address           Foreign Address         State      
tcp        0      0 0.0.0.0:5355            0.0.0.0:*               LISTEN     
tcp        0      0 0.0.0.0:2222            0.0.0.0:*               LISTEN     
tcp        0      0 100.115.92.205:8080     0.0.0.0:*               LISTEN     
tcp        0      0 127.0.0.53:53           0.0.0.0:*               LISTEN     
tcp        0      0 100.115.92.205:2222     100.115.92.25:42563     ESTABLISHED
tcp6       0      0 :::5355                 :::*                    LISTEN     
tcp6       0      0 :::2222                 :::*                    LISTEN     
tcp6       0      0 :::80                   :::*                    LISTEN     
udp        0      0 127.0.0.53:53           0.0.0.0:*                          
udp        0      0 0.0.0.0:68              0.0.0.0:*                          
udp        0      0 0.0.0.0:5355            0.0.0.0:*                          
udp6       0      0 :::5355                 :::*
````

`0.0.0.0` means web server is listening to every address available for requests.

If you stop the server and rerun `netstat -an | more`

````
Active Internet connections (servers and established)
Proto Recv-Q Send-Q Local Address           Foreign Address         State      
tcp        0      0 0.0.0.0:5355            0.0.0.0:*               LISTEN     
tcp        0      0 0.0.0.0:2222            0.0.0.0:*               LISTEN     
tcp        0      0 127.0.0.53:53           0.0.0.0:*               LISTEN     
tcp        0      0 100.115.92.205:2222     100.115.92.25:42563     ESTABLISHED
tcp6       0      0 :::5355                 :::*                    LISTEN     
tcp6       0      0 :::2222                 :::*                    LISTEN     
udp        0      0 127.0.0.53:53           0.0.0.0:*                          
udp        0      0 0.0.0.0:68              0.0.0.0:*                          
udp        0      0 0.0.0.0:5355            0.0.0.0:*                          
udp6       0      0 :::5355                 :::*
````
