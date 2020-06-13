FROM golang:1.14

RUN go get -v -d github.com/ava-labs/gecko/...

WORKDIR $GOPATH/src/github.com/ava-labs/gecko/

RUN ./scripts/build.sh

EXPOSE 9650

ENTRYPOINT [ "./build/ava" , "--public-ip=127.0.0.1", "--snow-sample-size=1", "--snow-quorum-size=1", "--staking-tls-enabled=false"]