FROM decentralizedcloud/golang-build-base:latest
LABEL maintainer="morteza.alizadeh@gmail.com"

RUN mkdir -p $GOPATH/src/temporary
WORKDIR $GOPATH/src/temporary
RUN go mod init
RUN go get -v -d -t github.com/onsi/ginkgo
RUN go get -v -d -t github.com/onsi/gomega
RUN go get golang.org/x/tools/cmd/cover
RUN go get github.com/mattn/goveralls

RUN rm -rf $GOPATH/src/temporary

