# dlbr-dockerapp

> Make your Docker Compose applications reusable, and share them on Docker Hub

```
$ docker-app render | docker-compose -f - up
```

If you prefer you can create a standalone configuration file to store those settings. Let's create prod.yml with the following contents:

```
version: 0.2.3
text: hello production
port: 4567
```

You can then run using that configuration file like so:

```
$ docker-app render -f prod.yml | docker-compose -f - up
```
