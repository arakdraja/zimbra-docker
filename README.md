# Zimbra Docker
## Downloading the image
The first step is to pull this image into your docker environment, for that just run the next:
```bash
docker pull jorgedlcruz/zimbra
```

## Creating Zimbra Containers
Now that we have an image called jorgedlcruz/zimbra, we can do a docker run with some special parameters, like this:
```bash
docker run -p 25:25 -p 80:80 -p 465:465 -p 587:587 -p 110:110 -p 143:143 -p 993:993 -p 995:995 -p 443:443 -p 8080:8080 -p 8443:8443 -p 7071:7071 -p 9071:9071 -h zimbra-docker.zimbra.io --dns 127.0.0.1 --dns 8.8.8.8 -i -t -e PASSWORD=Zimbra2017 jorgedlcruz/zimbra
```
As you can see we tell the container the ports we want to expose, and on which port, we also specify the container hostname, the password foir the Zimbra Administrator Account, and the image to use.

That's it! You can visit now the IP of your Docker Machine using HTTPS, or try the Admin Console with HTTPS and port 7071.

## Contribute to the Project
If you like to contribute to the project, you are free to do so, just fork the next repo https://github.com/jorgedlcruz/zimbra-docker and submit your changes.

## Other alternatives
You can still receiving updates and support for this particular project, from the original author, on the next GitHub repo (currently working on ZCS 8.7.11 and Ubuntu 16.04) - https://github.com/jorgedlcruz/zimbra-docker

There is another 2 maintained versions of Docker:
* For testing purposes we recommend the Zextras docker, multiple versions: https://hub.docker.com/r/zextras/zimbra8/
* For production purpose (work in progress), Zimbra docker from Zimbra upstream: https://github.com/Zimbra/zm-docker

