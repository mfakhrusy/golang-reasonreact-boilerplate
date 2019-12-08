# use alpine image 1.13.5-alpine
FROM golang:1.13.5-alpine

# install git bash and openssh
RUN apk update && apk upgrade && \
  apk add --no-cache bash git openssh

# set current working directory
WORKDIR /app/backend

# copy source code from current directory to container directory
COPY . . 

# build the app
RUN go build -o main .

# expose port
EXPOSE 8080

# run the app
CMD ["./main"]