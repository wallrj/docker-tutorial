FROM ubuntu:14.04
# Refer to the Dockerfile reference and extend this as required...
# https://docs.docker.com/reference/builder/
#
# `docker build --tag=docker-tutorial/sample2 .` to build an image,
# `docker images` to view the image information, and
# `docker run --rm --interactive --tty docker-tutorial/sample2 /bin/bash` to run the image interactively.
RUN apt-get update -y
RUN apt-get install -y fortune
ENTRYPOINT ["/usr/games/fortune"]
