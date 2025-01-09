# Stage 1: Build
# ใช้ Golang image
FROM golang:1.21.4 as build

# ตั้งค่า working directory
WORKDIR /workspace

# คัดลอก go.mod และ go.sum
COPY go.mod ./
COPY go.sum ./

# ดาวน์โหลด dependencies
RUN go mod download

# คัดลอกไฟล์โปรเจคทั้งหมด
COPY . .

# สร้าง binary
RUN go build -o /simple-crud-api

# เปิดพอร์ต 8000
# EXPOSE 8000

# คำสั่งเริ่มต้น
# CMD ["/simple-crud-api"]

# Stage 2: Production
FROM golang:1.21.4
WORKDIR /app
COPY --from=build /simple-crud-api ./
CMD ["/app/simple-crud-api"]