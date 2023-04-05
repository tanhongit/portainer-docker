# Portainer Docker Compose

Portainer is a tool that simplifies the management and maintenance of Docker’s containers. A simple setup to deploy Portainer using `docker-compose`.

[Portainer Source](https://github.com/portainer/portainer)

## Requirements
- Install [Docker](https://docker.io/)
- Install [Docker-compose](https://docs.docker.com/compose/install/)

## Clone this repository

Run:

```bash
git clone git@github.com:tanhongit/portainer-dockercompose.git
cd portainer-dockercompose/portainer-docker
```

## Modify env values in **.env** file

Change APP_NAME APP_PORT accordingly

Or using default values:

```
APP_NAME=portainer
APP_PORT=9001
```

## Setup

Run:

```bash
docker-compose up -d
```

## Check the network ID

Run:

```bash
docker ps
```

Check the Container ID of **`APP_NAME`-docker**.

Run the command:

```bash
docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <container ID>
```

`<container ID>`: Use the Container ID of **`APP_NAME`-docker**

You will get the IP address of this Container.

## Using

You can then access Portainer by using the IP address that you got it in step 4 over port 9000 with a web browser.

Example:

If the IP address is `172.18.0.2`, you can access Portainer by using the URL `http://172.18.0.2:9000`.
