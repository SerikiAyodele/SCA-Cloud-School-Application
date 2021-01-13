# Use Node base image
FROM node:alpine AS build

# Create app directory in Docker
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies in Docker
RUN npm ci

# Copy app from local environment into the Docker image
COPY . .

# Build the app
RUN npm run build

# Set the application's port number
EXPOSE 80

# Use Nginx base image
FROM nginx:alpine

# Copy build artifacts to Nginx folder for static hosting
COPY --from=build /usr/src/app/build /usr/share/nginx/html