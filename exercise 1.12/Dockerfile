FROM ubuntu:18.04

EXPOSE 5000

RUN apt-get update && apt-get install -y curl wget nano gnupg

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash -

RUN apt-get install -y nodejs

# RUN node -v && npm -v

WORKDIR /usr/src/app

COPY . .

RUN npm install
RUN npm run build
RUN npm install -g serve

CMD serve -s -l 5000 build