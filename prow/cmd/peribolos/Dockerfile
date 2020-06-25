FROM golang:1.14.0

RUN mkdir /infra
RUN mkdir /app
ADD . /infra/ 
WORKDIR /infra
RUN go build -o /app/peribolos /infra/prow/cmd/peribolos/main.go
WORKDIR /app
RUN rm -rf /infra

CMD ["/app/peribolos"]

