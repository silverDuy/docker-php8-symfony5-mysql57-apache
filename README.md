# Setup for Shopware6 App System
## Clone the source
```
 git clone git@github.com:shopwareLabs/dhl-app.git
```

## Setup ENV file
```
cp .env.example .env
```

## Run Docker Composer
```
docker-compose up -d --build
```

## SSH to the container
I assume that APP_NAME=foo
```
docker exec -it foo-server /bin/bash 
```