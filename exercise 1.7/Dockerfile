FROM ubuntu:20.04

WORKDIR /usr/src/app

COPY hello.sh .

# RUN chmod +x hello.sh
RUN apt-get update

RUN apt-get install curl -y

CMD ./hello.sh

