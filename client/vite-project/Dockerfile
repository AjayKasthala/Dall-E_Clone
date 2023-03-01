# Set the base image to Node.js
FROM node:16.13.2

# Set the working directory to /app
WORKDIR /app

# Copy the package.json and package-lock.json files for the client to the container
COPY package*.json ./

# Install the dependencies for the client
RUN npm install

# Copy the rest of the client files to the container
COPY . .

# Build the client application
RUN npm run build

# Expose the port the client will listen on
EXPOSE 5137

# Start the server
CMD ["npm", "run", "dev"]
