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

````
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 100.115.92.205  netmask 255.255.255.240  broadcast 100.115.92.207
        inet6 fe80::216:3eff:fe41:d8ee  prefixlen 64  scopeid 0x20<link>
        ether 00:16:3e:41:d8:ee  txqueuelen 1000  (Ethernet)
        RX packets 1409  bytes 709680 (693.0 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 431  bytes 69969 (68.3 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 4  bytes 200 (200.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 4  bytes 200 (200.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
````

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
