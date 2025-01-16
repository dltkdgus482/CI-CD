# Base image (ARM64 호환)
FROM --platform=linux/arm64 node:23.6.0-alpine AS build

# Set working directory
WORKDIR /app

# Install Corepack and enable Yarn Berry
RUN corepack enable && corepack prepare yarn@4.6.0 --activate

# Copy application files
COPY . .

# Initialize Yarn Berry and project folder
RUN yarn set version berry

# Install dependencies
RUN yarn install

# Build the application
RUN yarn build

# Expose the application port
EXPOSE 3000

# Start the application
CMD ["yarn", "dev"]
