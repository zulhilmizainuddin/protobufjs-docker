# protobufjs-docker [![Build Status](https://travis-ci.org/zulhilmizainuddin/protobufjs-docker.svg?branch=master)](https://travis-ci.org/zulhilmizainuddin/protobufjs-docker)

[protobufjs](https://www.npmjs.com/package/protobufjs) Docker image for compiling protobuf `proto` files into JavaScript.

Docker image based on Alpine Node.js image.

## Pull from Docker Hub

```
$ docker pull zulhilmizainuddin/protobufjs
```

## Build image locally

```
$ docker build -t zulhilmizainuddin/protobufjs .
```

## Compile proto file to JavaScript

```
$ docker run --rm -v $(pwd)/proto:/usr/src/proto zulhilmizainuddin/protobufjs pbjs -t static-module -w commonjs -o addressbook.js addressbook.proto
```

## Compile JavaScript to type definition file
```
$ docker run --rm -v $(pwd)/proto:/usr/src/proto zulhilmizainuddin/protobufjs pbts -o addressbook.d.ts addressbook.js
```