# Gunakan base image Go
FROM golang:1.22-alpine AS builder

# Set working directory
WORKDIR /app

# Copy semua file ke container
COPY . .

# Download dependencies
RUN go mod tidy

# Build aplikasi
RUN go build -o main .

# Stage final (lebih ringan)
FROM alpine:latest

WORKDIR /root/

# Copy binary dari stage builder
COPY --from=builder /app/main .

# Expose port API
EXPOSE 8080

# Jalankan aplikasi
CMD ["./main"]
