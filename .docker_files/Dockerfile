##### building stage #####
FROM ubuntu:22.04

# install package & g++ & gcc
RUN apt-get update &&\
    apt-get install -y \
    unzip \
    vim \
    fish\
    wget\
    curl\
    g++\
    gcc


# python package
RUN apt install python3.10 -y
RUN apt install python3-pip -y
RUN pip install --upgrade pip 
RUN pip install --no-cache-dir  -U \
    numpy\
    pandas\
    tensorflow\
    torch\
    matplotlib


# install mojo
RUN curl https://get.modular.com | \
  MODULAR_AUTH=mut_1f062679a4e34e0aa82d418a6c42fd4b \
  sh -
RUN modular clean & modular install mojo

RUN mkdir -p /root/src
