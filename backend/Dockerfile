#FROM golang:1.15.2
#FROM golang:1.17.7-alpine
#RUN apk update &&  apk add git
FROM golang:1.17.2


ENV GOPATH /go
ENV GO111MODULE on
COPY . /go/src/sample
WORKDIR /go/src/sample

RUN go install github.com/go-delve/delve/cmd/dlv@latest

RUN go install github.com/cosmtrek/air@latest
#RUN go get -u github.com/cosmtrek/air
#RUN go get github.com/cosmtrek/air@v1.29.0
#RUN go install github.com/cosmtrek/air@v1.27.3
#RUN go mod tidy && \
#    go install github.com/cosmtrek/air@v1.27.3
#RUN go get -u github.com/go-delve/delve/cmd/dlv
CMD ["air", "-c", ".air.toml"]**