## Docker Ruby && Sqlite


This repository contains **Dockerfile** of Ruby and Sqlite for [Docker](https://www.docker.io/)'s [trusted build](https://index.docker.io/u/dynaum/ruby-sqlite/) published to the public [Docker Registry](https://index.docker.io/).



### Installation

1. Install [Docker](https://www.docker.io/).

2. Download [trusted build](https://index.docker.io/u/dynaum/ruby-sqlite/) from public [Docker Registry](https://index.docker.io/): `docker pull dynaum/ruby-sqlite`

   (alternatively, you can build an image from Dockerfile: `docker build -t="dynaum/ruby-sqlite" github.com/dynaum/ruby-sqlite`)


### Usage

    docker run -it --rm dynaum/ruby-sqlite

