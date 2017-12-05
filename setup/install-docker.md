# Install Docker

## Required Steps

- [Install Git](/setup/install-git.md)

## Setup

### Uninstall Old Versions

```bash
$ sudo apt-get remove docker docker-engine docker.io
```

### Setup Repository

```bash
$ sudo apt-get update
$ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo apt-key fingerprint 0EBFCD88
$ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

### Install Docker CE

```bash
$ sudo apt-get update
$ sudo apt-get install docker-ce
$ sudo docker run hello-world
```

### Install Docker Compose

```bash
$ sudo curl -L https://github.com/docker/compose/releases/download/1.17.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
```

## Next Steps

None yet

## Back To The Beginning

- [Start Over](/README.md)

