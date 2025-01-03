FROM node:16.15-alpine3.14

# Set working directory
WORKDIR /opt/app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm ci

# Add non-root user and change ownership of application files
RUN adduser -S app && chown -R app /opt/app

# Copy the rest of the application files, including start.sh
COPY . . 

# Ensure the start.sh is executable
RUN chmod +x /opt/app/start.sh

# Ensure correct ownership for all files (including start.sh)
RUN chown -R app /opt/app

# Switch to a non-root user to run the application
USER app

# Expose the port your application will listen on
EXPOSE 3000

# Set ENTRYPOINT to the correct location for start.sh
ENTRYPOINT ["sh", "/opt/app/start.sh"]
