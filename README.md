# Portainer Docker Compose

Portainer is a tool that simplifies the management and maintenance of Docker’s containers. A simple setup to deploy Portainer using `docker-compose`

[Portainer Source](https://github.com/portainer/portainer)

## 1. Requirements
- Install [Docker](https://docker.io/)
- Install [Docker-compose](https://docs.docker.com/compose/install/)
- Clone this repository

Go to compose folder - run:
```
cd portainer-docker
```

## 2. Modify env values in **.env** file

Change APP_NAME APP_PORT accordingly

Or using default values:

```
APP_NAME=portainer
APP_PORT=9001
```

## 3. Setup

Run:
```
docker-compose up -d
```

## 4. Check the network ID

Run:
```
docker ps
```

Check the Container ID of **`APP_NAME`-docker**.

Run the command:
```
docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <container ID>
```

`<container ID>`: Use the Container ID of **`APP_NAME`-docker**

You will get the IP address of this Container.
  
## 5. Using

You can then access Portainer by using the IP address that you got it in step 4 over port 9000 with a web browser.
