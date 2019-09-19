FROM golang:1.13
LABEL maintainer="morteza.alizadeh@gmail.com"

RUN mkdir -p $GOPATH/src/temporary
WORKDIR $GOPATH/src/temporary
RUN go mod init
RUN go get -v -d -t github.com/go-kit/kit
RUN go get -v -d -t google.golang.org/grpc
RUN go get -v -d -t github.com/go-ozzo/ozzo-validation
RUN go get -v -d -t github.com/lucsky/cuid

RUN rm -rf $GOPATH/src/temporary

