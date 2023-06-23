# docker-arena

The official docker application for bee-queue arena.

You can `docker pull` Arena from [Docker Hub](https://hub.docker.com/r/mixmaxhq/arena).

To build the image simply run:

```shell
$ docker build -t <name-image> .
```

To build the image for IBM S390x architecture, run:

```shell
$ docker build -t <name-image> --build-arg IMAGE=s390x/node:lts-alpine .
```

To run a container, execute the following command. Note that we need to settle the location of `index.json` in this container via volume mounting:

```shell
$ docker run -p 4567:4567 -v </local/route/to/index.json>:/opt/arena/config.json <name-image>
```

Alternative way to run is to use `docker-compose`:

```shell
$ docker-compose up -d
```

See [the docs][usage] for `config.json`. Simple example also can be found in `example.config.json` file.

[usage]: https://github.com/bee-queue/arena/#usage
