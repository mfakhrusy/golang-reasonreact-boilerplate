FROM node:lts-alpine

# install git bash and openssh
RUN apk update && apk upgrade && \
  apk add build-base python

RUN npm -g install yarn

WORKDIR /app/frontend

COPY . .

RUN yarn install

RUN yarn build

EXPOSE 8000

CMD ["yarn", "start"]