# Hello world using gRPC

Guide is here: [gRPC-Web helloworld example](https://github.com/grpc/grpc-web/tree/master/net/grpc/gateway/examples/helloworld)

## How to run

Start first the Envoy container:

```bash
docker build -t helloworld/envoy -f ./envoy.Dockerfile .
docker run -d -p 8080:8080 helloworld/envoy
```

Run the server:

```bash
node server.js
```

Open the index.html with your favorite browser and contemplate the hello world.

## How to improve

Rebuild the client.js script using Webpack:

```bash
npx webpack client.js
```

## Issues on Windows 10

Using Docker for Windows, take note of [this commit](https://github.com/jdebarochez/hello-grpc/commit/f7322716b4e4d3e10eabf53de7ea90473bad676e) for your Envoy container to contact a service of your host machine. More information with this issue [gRPC-Web #402](https://github.com/grpc/grpc-web/issues/402).