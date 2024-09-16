FROM node:18

# Set the working directory
WORKDIR /opt/server/

# Expose the port the app runs on
EXPOSE 8080

# Set environment variables
ENV MONGO=true

# Copy package.json and install dependencies
COPY package.json ./
RUN npm install

# Copy the rest of the application code
COPY server.js ./

# Define the command to run the application
CMD ["node", "server.js"]
