# Gunakan base image untuk build
FROM golang:latest AS builder

# Set working directory di dalam container
WORKDIR /app

# Salin semua file ke dalam working directory
COPY . .

# Build aplikasi dengan menonaktifkan CGO
RUN CGO_ENABLED=0 GOOS=linux go build -o hello-kubernetes

# Gunakan base image minimal untuk menjalankan aplikasi
FROM alpine:latest

# Instal ca-certificates agar bisa menangani TLS
RUN apk --no-cache add ca-certificates

# Set working directory di dalam container
WORKDIR /root/

# Salin binary yang sudah dibuild dari builder
COPY --from=builder /app/hello-kubernetes .

# Pastikan file binary bisa dieksekusi
RUN chmod +x ./hello-kubernetes

# Jalankan aplikasi
CMD ["./hello-kubernetes"]
