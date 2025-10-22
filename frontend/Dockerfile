# Base image untuk build
FROM node:20-alpine AS builder

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

# Build project Vite
RUN npm run build

# Gunakan image ringan untuk serve hasil build
FROM nginx:alpine

# Copy hasil build ke direktori nginx
COPY --from=builder /app/dist /usr/share/nginx/html

# Expose port 3000
EXPOSE 3000

# Jalankan nginx
CMD ["nginx", "-g", "daemon off;"]
