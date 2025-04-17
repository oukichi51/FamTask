FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json (if available) and install dependencies
COPY package.json ./
RUN npm install

# Copy the rest of the application
COPY . .

# Build Tailwind CSS
RUN npx tailwindcss -i ./src/css/input.css -o ./dist/output.css

# Expose port and set default command
EXPOSE 8080
CMD ["npx", "http-server", "./app", "-c-1", "-p", "8080"]