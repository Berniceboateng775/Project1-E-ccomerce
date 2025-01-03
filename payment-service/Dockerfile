FROM node:16.15-alpine3.14

# Create application directory
RUN mkdir -p /opt/app

# Set working directory
WORKDIR /opt/app

# Copy the package files
COPY package*.json ./

# Install dependencies using npm ci
RUN npm ci

# Create non-root user for the app and adjust ownership
RUN adduser -S app
RUN chown -R app /opt/app

# Copy all other files (source code) into the container
COPY . .

# Set permissions for the application directory
RUN chown -R app /opt/app

# Switch to non-root user for running the application
USER app

# Expose application port
EXPOSE 3003

# Set the command to run the app
CMD ["npm", "run", "dev"]

