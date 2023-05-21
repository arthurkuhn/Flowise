FROM node:18-alpine

USER root

RUN apk add --no-cache libc6-compat
RUN apk add --no-cache git
RUN apk add --no-cache python3 py3-pip make g++

# Create app directory
WORKDIR /usr/src/app

# Bundle app source
COPY . .

RUN yarn install

RUN yarn build

EXPOSE 8080

CMD ["yarn", "start"]