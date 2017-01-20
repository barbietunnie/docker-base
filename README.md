Tiny base image that can be used as the base for microcontainers. Currently, it's just the alpine OS image.

The inspiration for this was obtained from [Iron.io Uber tiny docker images](https://github.com/iron-io/dockers)

## Building this image

First, be sure to get the latest alpine:

```sh
docker pull alpine
docker pull alpine:edge
```

Then build it:

```sh
docker build -t barbietunnie/base:latest --no-cache .
```

Tag it with Alpine version, run `docker run --rm barbietunnie/base cat /etc/os-release` to check version.

```sh
docker tag barbietunnie/base:latest barbietunnie/base:X.Y.Z
```

Push:

```sh
docker push barbietunnie/base
```
