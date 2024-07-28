# Use the official Node.js image as a base
FROM node:18-slim

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json (if available)
COPY ./package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose port 8080 for the API server
EXPOSE 8080

# Command to run the application
CMD ["npm", "run", "start"]
