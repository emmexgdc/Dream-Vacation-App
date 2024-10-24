# Use Node.js LTS version as the base image
FROM node:18-slim

# Set working directory
WORKDIR /usr/src/app/backend

# Copy package files
COPY backend/package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the backend code
COPY backend/ ./

# Create .env file from example if it doesn't exist
COPY backend/.env.example ./.env

# Expose the port your app runs on
ENV PORT=3001
EXPOSE $PORT

# Command to run the application
CMD ["npm", "start"]