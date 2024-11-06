# Use Node.js LTS version
FROM node:16-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json
COPY package.json package-lock.json ./

# Install dependencies
RUN npm ci --only=production

# Copy the rest of your application's source code
COPY . .

# Expose the port PartyKit runs on (change if different)
EXPOSE 3000

# Start the PartyKit application
CMD ["npm", "deploy"]
