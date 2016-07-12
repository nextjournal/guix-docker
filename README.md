# guix-docker
Dockerfile for GNU Guix

Rest of the readme and the Dockerfile copied from: https://github.com/bmpvieira/Dockerfiles

Licensed under the GNU General Public License version 3 or later. Some of the code/docs are under the MIT license.

# Guix

Guix requires ```--privileged``` to run.

```bash
docker run -ti --privileged bmpvieira/guix:pull
guix-daemon --build-users-group=guix-builder &
guix pull
```

[Guix pull](https://www.gnu.org/software/guix/manual/html_node/Invoking-guix-pull.html) takes a while and [cannot be added to the Dockerfile](https://github.com/docker/docker/issues/1916) since it requires ```--privileged```. However, you can fetch a Docker image pushed to the [Docker hub](https://hub.docker.com/r/bmpvieira/guix/tags/) after this step was already performed by using the tag ```pull```.

```bash
docker run -ti --privileged bmpvieira/guix:pull
```
