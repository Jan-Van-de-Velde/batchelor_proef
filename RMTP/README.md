# RMTP

## Wat is RMTP

## waarom gebruik ik RMPT

## installatie RMTP server voor nginx

* stap 1:- sudo apt update
* stap 2:- sudo apt install nginx
* stap 3:- sudo apt install libnginx-mod-rtmp
* stap 4:- sudo systemctl start nginx
* stap 5:- sudo systemctl enable nginx
* stap 6:- sudo nano /etc/nginx/nginx.conf 
* stap 7:- voeg onderstaande lijnen toe /etc/nginx/nginx.conf (Save Ctrl+x)
```
rtmp {
        server {
                listen 1935;
                chunk_size 4096;
                allow publish all;

                application live {
                        live on;
                        record off;
                }
        }
}
```
* stap 8:- verzorg network communicatie tussen RMTP server en drone die beelden produceert.