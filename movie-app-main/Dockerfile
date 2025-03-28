# Step 1: Use Node.js to build the React app
FROM node:18-alpine AS build

# Set the working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the project files
COPY . .

# Build the React app
RUN npm run build

# Expose the Vite preview port (default is 4173)
EXPOSE 4173

# Start the Vite preview server
CMD ["npm", "run", "preview", "--", "--host"]