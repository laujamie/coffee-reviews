FROM golang:1.17 as base

WORKDIR /app
COPY . .

RUN go get -d -v

FROM base as dev

RUN curl -sSfL https://raw.githubusercontent.com/cosmtrek/air/master/install.sh | sh -s -- -b $(go env GOPATH)/bin

CMD ["air"]
