# M901

Unsere Applikation ist ...
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

Say what the step will be

```
Give the example
```

And repeat

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

## Built With



## Contributing



## Versioning



## Authors


## License


## Acknowledgments

