Install Docker Machine on MacOSX
--------------------------------

Instructions for installing docker-machine and the docker client on MacOSX.

### Install Virtualbox
Download and install virtualbox so we can start virtual machines - [Link here](https://www.virtualbox.org/wiki/Downloads)

### Install the Docker CLI
This grabs a copy of the docker client binary so we can type `docker` on our Mac.

```bash
$ cd ~
$ curl -o docker http://get.docker.io/builds/Darwin/x86_64/docker-latest
$ chmod +x ./docker
$ mv docker ~/bin
```

### Install Docker Machine
This grabs a copy of the docker machine binary so we can use it to create new docker based virtual machines.

```bash
$ cd ~
$ curl -o docker-machine https://github.com/docker/machine/releases/download/v0.1.0/docker-machine_darwin-amd64
$ chmod +x ./docker-machine
$ mv docker-machine ~/bin
```

Test this worked by typing:

```bash
$ docker-machine -v
```

### Create Docker VM
We use docker-machine to spin up a new virtualbox VM with docker installed:

```bash
$ docker-machine create --driver virtualbox dev
```

Check the box exists:

```bash
$ docker-machine ls
```

### Export variables
Export the env variables to connect to the docker box

```bash
$ eval "$(docker-machine env dev)"
```

Test that the docker client is now connected to our new server:

```bash
$ docker ps
```

### Run a container

```bash
$ docker run busybox echo hello world
```

### Stop box

```bash
$ docker-machine stop dev
$ docker-machine ls
```

### Help

[the docs are here](https://docs.docker.com/machine/)