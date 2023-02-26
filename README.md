# Docker cron image

**Duktig Microservices** - Docker cron image based on Ubuntu GNU/Linux

## Version 1.1.0

>NOTE: To install php-cli in this image, uncomment the line in `Dockerfile` :

```
RUN apt-get install php-cli -y
``` 

## Build image 

    $ cd path/to/this/directory

    $ sudo docker build --rm -t docker-cron . 

Run the docker container in the background (docker returns the id of the container):

    $ sudo docker run -t -i -d docker-cron

View running containers

    $ sudo docker ps

Check if the container deployed properly

> NOTE: Remember to change container-id
 
    $ sudo docker exec -i -t {container-id} /bin/bash
    
    root@b149b5e7306d:/# cat /var/log/cron.log
  

## Modify the cron file

Tp change the cron file you have to edit the `/etc/cron.d/simple-cron` inside container or the file `simple-cron` before building the image.

`* * * * * root /script.sh`

## Credits

This Installation schema is a part of **Duktig Microservices** Package developed by **Duktig Solutions LLC**

**Copyright 2021 Duktig Solutions LLC**

## Contacts

- Email: software@duktig.dev>
- Phone: +37495565003
- Website: http://duktig.solutions

End of document
