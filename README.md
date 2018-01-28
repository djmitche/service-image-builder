# service-image-builder

Playground for building images for microservices

# Usage

```sh
./bin/build-service <repository> <reference>
```
e.g:

```sh
./bin/build-service https://github.com/taskcluster/taskcluster-auth master
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
## Troubleshooting

+ under OSX, you may want to configure shared paths from `Docker -> Preferences... -> File Sharing` tp add `/var/folders` into your shared paths of Docker.

+ unset PYTHONPATH if you get AttributeError: module 'enum' has no attribute 'IntFlag'. [see https://stackoverflow.com/a/42214539 for more detail]