# M901

Unsere Applikation ist ein Web Shop
# Project Title

One Paragraph of project description goes here

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

```
Give examples
```

### Installing

A step by step series of examples that tell you how to get a development env running
```
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs	
```
```
git clone https://github.com/ZeroFuntom/M901.git
```
```
sudo chmod -R 777 M901
cd ~/M901/src/client/shop
npm install
cd src/app
npm start
```
```
until finished
```



## Running the tests



### Break down into end to end tests


```
Give an example
```

### And coding style tests


```
Give an example
```

## Deployment
Dockerfile
```
FROM node:8

# Create app directory
WORKDIR /Users/Data/M901/src/client/

COPY shop ./

RUN npm config set registry http://registry.npmjs.org/
RUN npm install

EXPOSE 4200

CMD [ cd /src/app | npm start ]

```
Image wird erstellt.
```
docker build -t node-web-app .
```
Container wird erstellt und gestartet
```
docker run -p 4200:4200 -d node-web-app
```
Auf den Container verbinden.
```
docker exec -it 1551cea5029c /bin/bash
```
Überprüfen ob der Webshop funktioniert.
```
curl localhost:4200
```
Antwort wenn localhost geöffnet wird
```
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Onlineshop</title>
  <base href="/">

  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="icon" type="image/x-icon" href="favicon.ico">
</head>
<body>
  <pm-root></pm-root>
<script type="text/javascript" src="inline.bundle.js"></script><script type="text/javascript" src="polyfills.bundle.js"></script><script type="text/javascript" src="styles.bundle.js"></script><script type="text/javascript" src="vendor.bundle.js"></script><script type="text/javascript" src="main.bundle.js"></script></body>
</html>
```
## Built With



## Contributing



## Versioning



## Authors


## License


## Acknowledgments

