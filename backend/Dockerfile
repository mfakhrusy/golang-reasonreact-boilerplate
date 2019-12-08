# use alpine image 1.13.5-alpine
FROM golang:1.13.5-alpine

# install git bash and openssh
RUN apk update && apk upgrade && \
  apk add --no-cache bash git openssh

# set current working directory
WORKDIR /app/backend

COPY . . 

RUN go build -o main .

EXPOSE 8080

CMD ["./main"]