# Specify a bas image
FROM node:alpine

# Create and set folder to place our code
WORKDIR /usr/src

# Copy the sources
COPY . /usr/src

# Install some depenedencies
RUN npm install

# Default command
CMD ["npm", "start"]