FROM golang:1.13.4
LABEL maintainer="morteza.alizadeh@gmail.com"

RUN apt-get update -y
RUN apt-get install unzip

ENV PROTOC_ZIP=protoc-3.10.1-linux-x86_64.zip
RUN curl -OL https://github.com/google/protobuf/releases/download/v3.10.1/$PROTOC_ZIP
RUN unzip -o $PROTOC_ZIP -d /usr/local bin/protoc
RUN unzip -o $PROTOC_ZIP -d /usr/local include/*
RUN rm -f $PROTOC_ZIP

ENV GIT_TAG="v1.3.2"
RUN go get -d -u github.com/golang/protobuf/protoc-gen-go
RUN git -C "$(go env GOPATH)"/src/github.com/golang/protobuf checkout $GIT_TAG
RUN go install github.com/golang/protobuf/protoc-gen-go

RUN apt-get clean

