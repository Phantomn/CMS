# Use an official Node.js runtime as the base image
FROM node:22

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json
COPY package*.json ./
COPY prisma ./

# Install dependencies
RUN npm install --legacy-peer-deps

# Copy the rest of the application code
COPY . .

# Build the application (if applicable)
# RUN npm run build

# Expose the application's port
EXPOSE 8888

# Start the application
CMD ["npm", "run", "dev"]
