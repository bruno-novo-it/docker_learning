# Use an official node runtime as a parent image
FROM node:12.8.1-alpine

# Make /app the default working directory
WORKDIR /app/

# Copy package.json to the container
COPY ./frontend/package.json /app/

# Install all needed dependencies
RUN npm install \
    npm install -g @angular/cli@6.1.4

# Add rest of the code
COPY ./frontend/ /app/

# Expose the port to external access
EXPOSE 4200

# Run the Application(Develop)
CMD ng serve --host 0.0.0.0