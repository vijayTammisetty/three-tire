# Use the official Node.js image
FROM node:16-slim

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json (for npm)
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy the entire React project into the container
COPY . .

# Build the React app for production
# RUN npm run build

# Install a simple HTTP server to serve the React build files
# RUN npm install -g serve

# Expose the port the React app will run on (default React port is 3000)
EXPOSE 3000

# Serve the React build folder using the "serve" package
CMD ["npm", "start"]
