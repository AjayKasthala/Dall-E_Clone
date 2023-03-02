#Set the base image to Node.js
FROM node:14-alpine

# Set the working directory to /app
WORKDIR /app

# Copy the package.json and package-lock.json files for the server to the container
COPY package*.json ./

# Install the dependencies for the server
RUN npm install

# Copy the rest of the server files to the container
COPY . .

# Build the server application
RUN yarn

# Expose the port the server will listen on
EXPOSE 8080

# Start the server
CMD ["npm", "start"]