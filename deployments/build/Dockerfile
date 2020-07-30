FROM golang:alpine
RUN apk update && apk add --no-cache git
WORKDIR $GOPATH/src
COPY cmd/pinger .
RUN go get -d -v && go build -o /go/bin/pinger
ENTRYPOINT ["pinger"]
