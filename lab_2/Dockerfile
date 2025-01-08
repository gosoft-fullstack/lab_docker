# Stage 1: Build
FROM golang:1.23 as build
WORKDIR /app
COPY . .
RUN go build -o api ./main.go

# Stage 2: Production
FROM alpine:latest
WORKDIR /app
COPY --from=build /app/api .
CMD ["/app/api"]