FROM golang:1.20-alpine as builder

ENV TZ=Asia/Shanghai

RUN apk --update add gcc musl-dev linux-headers git

WORKDIR /build

COPY ./ ./
RUN go mod download
COPY *.go ./

RUN  go build  -ldflags="-w -s"

FROM alpine:3

WORKDIR /app

RUN apk update --no-cache && apk upgrade

COPY --from=builder /build/hahajing /app/hahajing
COPY ./config /app/config

EXPOSE 80
CMD ["nohup", "./hahajing", "server"]
