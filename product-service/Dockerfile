FROM node:16.15-alpine3.14

# Set working directory
WORKDIR /opt/app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm ci

# Add non-root user and change ownership
RUN adduser -S app && chown -R app /opt/app

# Copy remaining application files
COPY . .

# Set permissions and switch user
RUN chown -R app /opt/app
USER app

# Expose the desired port
EXPOSE 3001

# Run the application
CMD ["npm", "run", "dev"]
