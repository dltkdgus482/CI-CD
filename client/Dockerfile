# Base image
FROM node:23.6.0-alpine AS build

# Set working directory
WORKDIR /app

# Copy application files
COPY . .

# Install dependencies
RUN yarn install --ignore-engines

# Build the application
RUN yarn build

# Expose the application port
EXPOSE 3000

# Start the application
CMD ["yarn", "start"]
