From ubuntu:18.04

EXPOSE 8080

RUN apt-get update && apt-get install -yqq curl wget nano gnupg

RUN wget https://go.dev/dl/go1.20.7.linux-amd64.tar.gz && tar -C /usr/local -xzf go1.20.7.linux-amd64.tar.gz

ENV PATH=$PATH:/usr/local/go/bin

RUN go version

WORKDIR /usr/src/app

COPY . .

RUN go build
RUN go test ./...
CMD ./server
