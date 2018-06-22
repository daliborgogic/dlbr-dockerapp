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

## Installation

```bash
wget https://github.com/docker/app/releases/download/v0.2.0/docker-app-linux.tar.gz
tar xf docker-app-linux.tar.gz
cp docker-app-linux /usr/local/bin/docker-app
```

## Usage

```
$ docker-app
Docker App Packages

Usage:
  docker-app [command]

Available Commands:
  helm        Render the Compose file for this app as an Helm package
  help        Help about any command
  init        Initialize an app package in the current working directory
  inspect     Retrieve metadata for a given app package
  render      Render the Compose file for this app
  version     Print version information

Flags:
  -h, --help   help for docker-app

Use "docker-app [command] --help" for more information about a command.
```
