# Use a lightweight Node.js base image
FROM node:18-slim AS builder

# Set the working directory
WORKDIR /usr/src/app

# Copy package files first for dependency installation
COPY package*.json ./

# Install only production dependencies
RUN npm install --only=production

# Copy the application code
COPY . .

# Expose the application port
EXPOSE 3002

# Command to run the application
CMD ["node", "app.js"]
