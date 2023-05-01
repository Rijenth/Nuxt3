FROM node:18-alpine

WORKDIR /frontend

RUN apk update && apk upgrade

RUN apk add git

COPY ./package*.json /frontend/

RUN yarn install && yarn cache clean --force

COPY . .

ENV PATH ./node_modules/.bin/:$PATH