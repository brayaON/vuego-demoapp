FROM golang:1.15
WORKDIR /go/src/backend
COPY . .
RUN go build -o backend
EXPOSE 4000
CMD ["./backend"]