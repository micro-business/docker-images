FROM ubuntu:18.04
LABEL maintainer="morteza.alizadeh@gmail.com"

RUN apt-get update -y
RUN apt-get install -y --no-install-recommends curl git

RUN curl --insecure -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
RUN chmod +x ./kubectl
RUN mv ./kubectl /usr/local/bin/

RUN curl --insecure -Lo ./helm.tar.gz https://get.helm.sh/helm-v3.1.0-linux-amd64.tar.gz
RUN mkdir ./helm
RUN tar -C ./helm -xzf helm.tar.gz
RUN mv ./helm/linux-amd64/helm /usr/local/bin/
RUN rm -rf ./helm
RUN rm -rf helm.tar.gz

RUN apt-get clean

