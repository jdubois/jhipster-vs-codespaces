FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu-18.04

RUN \
  apt-get update && \
  apt-get install -y \
    software-properties-common \
    docker-compose && \
  apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 0xB1998361219BD9C9 && \
  apt-add-repository 'deb http://repos.azulsystems.com/ubuntu stable main' && \
  apt-get update && \
  apt-get install -y zulu-11 && \
  # cleanup
  apt-get clean
