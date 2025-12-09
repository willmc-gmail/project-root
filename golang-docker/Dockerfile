
# 使用官方 Golang 映像檔
FROM golang:1.21-alpine

# 設定工作目錄
WORKDIR /app

# 複製檔案
COPY . .

# 編譯程式
RUN go build -o main .

# 啟動服務
CMD ["./main"]
