# Sử dụng image Node.js làm base image
FROM node:14-alpine

# Tạo thư mục làm việc
WORKDIR /app

# Sao chép package.json và package-lock.json vào image
COPY package*.json ./

# Cài đặt dependencies
RUN npm install

# Sao chép toàn bộ code frontend vào image
COPY . .

# Build ứng dụng React
RUN npm run build

# Expose port 5173 vite
EXPOSE 5173

# Chạy ứng dụng bằng npm
CMD ["npm", "run", "preview"]