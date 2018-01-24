# service-image-builder

Playground for building images for microservices

# Usage

```sh
./bin/build-service <repository> <reference>
```

## Repository Requirements

The repository can optionally have a `.build-config.sh` in its root, containing:

```
# values shown are the defaults
BUILD_TYPE=heroku-buildpack
HEROKU_STACK=heroku-16
# buildpack must *always* be a URL or URL#ref; heroku's shorthands are not supported
HEROKU_BUILDPACK=https://github.com/heroku/heroku-buildpack-nodejs#master
```
