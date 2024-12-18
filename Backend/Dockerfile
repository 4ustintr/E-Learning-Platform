# Sử dụng image Node.js làm base image
FROM node:14-alpine

# Tạo thư mục làm việc
WORKDIR /app

# Sao chép package.json và package-lock.json vào image
COPY package*.json ./

# Cài đặt dependencies
RUN npm install

# Sao chép toàn bộ code backend vào image
COPY . .

# Expose port 5000
EXPOSE 8080

# Chạy ứng dụng Node.js
CMD ["node", "server.js"]