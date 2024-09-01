#Build Stage
FROM golang:alpine AS builder
WORKDIR /go/src/app
COPY src/ .
WORKDIR /go/src/app/main
RUN go get -v ./...
RUN go build -o /go/bin/app -v ./...

#Final Stage
FROM alpine
WORKDIR /auth-app
RUN apk --no-cache add ca-certificates
COPY --from=builder /go/bin/app .
EXPOSE 8080
LABEL Name="auth" Version="0.0.1"
ENTRYPOINT [ "/app/auth" ]