![mailhog 1.0.x](https://img.shields.io/badge/mailhog-1.0.x-green.svg)

![WPLib-Box](https://github.com/wplib/wplib.github.io/raw/master/WPLib-Box-100x.png)


# MailHog Docker Container for WPLib Box
This is the repository for the [MailHog](https://github.com/mailhog/MailHog) Docker container implemented for [WPLib-Box](https://github.com/wplib/wplib-box).
It currently provides versions 1.0.x


## Supported tags and respective Dockerfiles

`1.0.0`, `1.0`, `latest` _([1.0.0/Dockerfile](https://github.com/wplib/mailhog-docker/blob/master/1.0.0/Dockerfile))_


## Using this container.
If you want to use this container as part of WPLib, then use the Docker Hub method.
Or you can use the GitHub method to build and run the container.


## Using it from Docker Hub

### Links
(Docker Hub repo)[https://hub.docker.com/r/wplib/mailhog/]

(Docker Cloud repo)[https://cloud.docker.com/swarm/wplib/repository/docker/wplib/mailhog/]


### Setup from Docker Hub
A simple `docker pull wplib/mailhog` will pull down the latest version.


### Runtime from Docker Hub
start - Spin up a Docker container with the correct runtime configs.

`docker run -d --name wplib_mailhog_1.0.0 --restart=always --network wplibbox -p 8025:8025 -p 1025:1025  wplib/mailhog:1.0.0`

stop - Stop a Docker container.

`docker stop wplib_mailhog_1.0.0`

run - Run a Docker container in the foreground, (all STDOUT and STDERR will go to console). The Container be removed on termination.

`docker run --rm --name wplib_mailhog_1.0.0 --network wplibbox -p 8025:8025 -p 1025:1025  wplib/mailhog:1.0.0`

shell - Run a shell, (/bin/bash), within a Docker container.

`docker run --rm --name wplib_mailhog_1.0.0 -i -t --network wplibbox -p 8025:8025 -p 1025:1025  wplib/mailhog:1.0.0 /bin/bash`

rm - Remove the Docker container.

`docker container rm wplib_mailhog_1.0.0`


## Using it from GitHub repo

### Setup from GitHub repo
Simply clone this repository to your local machine

`git clone https://github.com/wplib/mailhog-docker.git`


### Building from GitHub repo
`make build` - Build Docker images. Build all versions from the base directory or specific versions from each directory.


`make list` - List already built Docker images. List all versions from the base directory or specific versions from each directory.


`make clean` - Remove already built Docker images. Remove all versions from the base directory or specific versions from each directory.


`make push` - Push already built Docker images to Docker Hub, (only for WPLib admins). Push all versions from the base directory or specific versions from each directory.


### Runtime from GitHub repo
When you `cd` into a version directory you can also perform a few more actions.

`make start` - Spin up a Docker container with the correct runtime configs.


`make stop` - Stop a Docker container.


`make run` - Run a Docker container in the foreground, (all STDOUT and STDERR will go to console). The Container be removed on termination.


`make shell` - Run a shell, (/bin/bash), within a Docker container.


`make rm` - Remove the Docker container.


`make test` - Will issue a `stop`, `rm`, `clean`, `build`, `create` and `start` on a Docker container.


