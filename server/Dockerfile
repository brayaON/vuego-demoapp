FROM golang:1.15
WORKDIR /go/src/backend
ENV PORT=4001
EXPOSE 4000 ${PORT}
COPY . .
RUN go build -o backend
CMD ["./backend"]