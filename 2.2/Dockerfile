# Pull base image.
FROM ubuntu:14.04
MAINTAINER Dynaum

# Ignore APT warnings about not having a TTY
ENV DEBIAN_FRONTEND noninteractive

# dependencies
RUN \
  apt-get update && \
  apt-get -y install \
  build-essential \
  curl \
  git-core \
  libcurl4-openssl-dev \
  libc6-dev \
  libreadline-dev \
  libssl-dev \
  libxml2-dev \
  libxslt1-dev \
  libyaml-dev \
  zlib1g-dev \
  libssl-dev \
  imagemagick

# Ruby install
RUN \
  curl --progress http://cache.ruby-lang.org/pub/ruby/2.2/ruby-2.2.3.tar.gz | tar xz && \
  cd ruby-2.2.3 && \
  ./configure --disable-install-doc && \
  make && make install && \
  cd .. && rm -rf ruby-2.2.3* && \
  echo 'gem: --no-document' > /usr/local/etc/gemrc && \
  gem install bundler

# SqLite
RUN apt-get -y install sqlite3 libsqlite3-dev

# Set locale
RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

CMD "bash"
