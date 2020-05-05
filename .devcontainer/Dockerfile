FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu-18.04

# Avoid warnings by switching to noninteractive
ENV DEBIAN_FRONTEND=noninteractive

# Configure apt and install packages
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

# Switch back to dialog for any ad-hoc use of apt-get
ENV DEBIAN_FRONTEND=dialog
