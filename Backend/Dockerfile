# Sử dụng image Node.js làm base image
FROM node:22.9.0-alpine

# Tạo thư mục làm việc
WORKDIR /app

RUN npm install -g npm@latest
# Sao chép package.json và package-lock.json vào image
COPY package*.json ./

# Cài đặt dependencies
RUN npm install

# Sao chép toàn bộ code backend vào image
COPY . .

# Expose port 8080
EXPOSE 8080

# Chạy ứng dụng Node.js
CMD ["node", "server.js"]