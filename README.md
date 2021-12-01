# ncWebServer
**netcat as a mini webserver**
>To retrieve some info in a local network via a browser, it is not always necessary to install a big web server like Apache or nginX. The Linux tool nc can do that too.

tested on Ubuntu 20.04  
  
on a machine which has e.g. the IP 192.168.178.100, execute the following in the terminal:  
`while true; do echo -e "HTTP/1.1 200 OK\n\n $(date)" | nc -l 8080 -q 1; done`  

and run it on another machine on the same network  
- in the Terminal: curl 192.168.178.100:8080  
- or in Browser: 192.168.178.100:8080  

With this you have a small one-line web server running.
