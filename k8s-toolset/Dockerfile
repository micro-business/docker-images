FROM ubuntu:20.04
LABEL maintainer="morteza.alizadeh@gmail.com"

RUN apt-get update -y && apt-get install -y --no-install-recommends ca-certificates apt-transport-https gnupg2 curl git
RUN curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key add -
RUN echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | tee -a /etc/apt/sources.list.d/kubernetes.list
RUN apt-get update
RUN apt-get install -y --no-install-recommends kubectl

RUN curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
RUN chmod 700 get_helm.sh
RUN ./get_helm.sh
RUN rm -f ./get_helm.sh

RUN apt-get clean

