---
title: "Docker CLI"
date: 2019-09-21T17:56:32+02:00
draft: false
---

See [Documentation](https://docs.docker.com/engine/reference/commandline/docker/).

## Usual commands

Command | Action
------- | ------
`docker ps` | Get all running containers
`docker ps --all` | Get all containers
`docker rm <containerid>` | Delete a container by its id
`docker images` | Get all images on the system
`docker version` | Get Docker version
`docker info` | Get Docker general information
`docker run hello-world` | Run Hello world image
`docker run -it ubuntu bash` | Run Ubuntu image with an interactive shell
`docker network ls` |
`docker network inspect bridge` |
`docker exec -it <containerid> sh` |

See [Docker Cheat Sheet from Will Sargent](https://github.com/wsargent/docker-cheat-sheet).
