# Ubuntu 16.04 LTS (Xenial) MDSK Test Image

Ubuntu 16.04 LTS (Xenial) Docker container for MDSK testing.

## How to Build

This image is built on Docker Hub automatically any time the upstream OS container is rebuilt, and any time a commit is made or merged to the `master` branch. But if you need to build the image on your own locally, do the following:

  1. [Install Docker](https://docs.docker.com/engine/installation/).
  2. `cd` into this directory.
  3. Run `docker build -t ubuntu1604-mdsk .`

## How to Use

  1. [Install Docker](https://docs.docker.com/engine/installation/).
  2. Pull this image from Docker Hub: `docker pull kporras07/docker-ubuntu1604-mdsk:latest` (or use the tag you built earlier, e.g. `ubuntu1604-mdsk`).
  3. Run a container from the image: `docker run --detach --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro kporras07/docker-ubuntu1604-mdsk:latest /usr/lib/systemd/systemd`

## Author

Created in 2016 by Kevin Porras; based on ubuntu1604-ansible by [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).
