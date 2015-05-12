# zeitgeist/docker-midori

Lightweight browser [midori](http://midori-browser.org/) in a Docker container.

## Requirements

* [Docker](https://www.docker.com/) 1.5+ (previous versions may work fine, but I haven't tried)
* An X11 socket

## Installation

Get the [trusted build on the docker hub](https://registry.hub.docker.com/u/zeitgeist/docker-midori/):

```bash
$ docker pull zeitgeist/docker-midori
```

or download and compile the source yourself from Github:

```bash
$ git clone https://github.com/alexzeitgeist/docker-midori.git
$ cd docker-midori
$ docker build -t zeitgeist/docker-midori .
```

## Usage

```bash
$ docker run --rm \
  -v /tmp/.X11-unix:/tmp/.X11-unix:ro \
  -e DISPLAY=unix$DISPLAY \
  zeitgeist/docker-midori
```
