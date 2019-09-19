FROM decentralizedcloud/golang-build-base:latest
LABEL maintainer="morteza.alizadeh@gmail.com"

RUN mkdir -p $GOPATH/src/temporary
WORKDIR $GOPATH/src/temporary
RUN go mod init
RUN go get -v -d -t github.com/onsi/ginkgo
RUN go get -v -d -t github.com/onsi/gomega
RUN go get -v -t github.com/mattn/goveralls
RUN go get -v -t github.com/modocache/gover

RUN rm -rf $GOPATH/src/temporary

