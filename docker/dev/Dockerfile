FROM ubuntu:latest

#ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update
RUN apt-get install -y curl build-essential make gcc sudo git rsync bash

RUN sh -ci "$(curl -sL https://deb.nodesource.com/setup_14.x)"
RUN apt-get install -y nodejs

#RUN apt-get install -y tree zsh less
RUN apt-get clean

# DFX
RUN echo yes | sh -ci "$(curl -fsSL https://sdk.dfinity.org/install.sh)"

#
## Oh my zsh
#RUN sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
