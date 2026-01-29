FROM node:18-alpine

# Create app directory
WORKDIR /app

# Copy only package files first (better caching)
COPY package*.json ./

# Install dependencies
RUN npm install --legacy-peer-deps

# Copy rest of backend code
COPY . .

# Expose backend port (change if your app uses another)
EXPOSE 5000

# Start backend
CMD ["node", "index.js"]
