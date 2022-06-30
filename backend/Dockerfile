FROM golang:1.17-alpine

WORKDIR /go/src/app
COPY . .

RUN go get -d -v
RUN go build -v -o main

CMD ["./main"]
