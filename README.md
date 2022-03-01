# Portainer Docker Compose

Portainer is a tool that simplifies the management and maintenance of Docker’s containers.

## 1. Modify env values in **.env** file

Change APP_NAME APP_PORT accordingly

```
APP_NAME=portainer
APP_PORT=9001
```

## 2. Setup
Go to compose folder - run:
```
cd portainer-docker
```

Then run:
```
docker-compose up -d
```

## 3. Check the network ID

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
  
 
