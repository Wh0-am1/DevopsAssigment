FROM golang:alpine
RUN apk add --no-cache curl
COPY . /app
WORKDIR /app
CMD ["go" , "run","main.go"]
