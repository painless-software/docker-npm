npm
===

[![dockeri.co](http://dockeri.co/image/painless/npm)](https://hub.docker.com/r/painless/npm/)

[![MIT License](https://img.shields.io/github/license/painless-software/docker-npm.svg)](https://github.com/painless-software/docker-npm/blob/master/LICENSE
) [![GitHub issues](https://img.shields.io/github/issues-raw/painless-software/docker-npm.svg)](https://github.com/painless-software/docker-npm/issues
) [![GitHub PRs](https://img.shields.io/github/issues-pr-raw/painless-software/docker-npm.svg)](https://github.com/painless-software/docker-npm/pulls)

Node Package Manager
--------------------

Convenience wrapper around the well-known JavaScript runtime package manager, for local development with [Docker Compose](
https://docs.docker.com/compose/) and anything that runs on [Node.js](https://nodejs.org/). Extends the official [`node`](
https://hub.docker.com/r/_/node/) image with a customizable entrypoint to run executables of node modules.

Supported Tags
--------------

- [`latest`](https://github.com/painless-software/docker-npm/blob/master/Dockerfile) [![Image Layers](
  https://img.shields.io/imagelayers/layers/painless/npm/latest.svg)](https://imagelayers.io/?images=painless/npm:latest
  ) (node base image with adapted entrypoint)

Usage
-----

Add a pseudo-service to your Docker Compose configuration, e.g.

```
  npm:
    image: painless/npm
    volumes:
      - .:/var/www/html
```

then run

```
docker-compose run npm <command>
```

to let npm modify the project files on your Docker volume.

See [docker-compose.override.yml](
https://github.com/painless-software/painless-continuous-delivery/blob/master/%7B%7Bcookiecutter.project_slug%7D%7D/_/deployment/php/docker-compose.override.yml
) in the [Painless Continuous Delivery cookiecutter](https://github.com/painless-software/painless-continuous-delivery) for an example.

Development
-----------

- [Contribute](https://github.com/painless-software/docker-npm/) (GitHub repository)
