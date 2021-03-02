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

# If we bind our application to listen to a specific url, like localhost, it will not work. Because the container 
# does not share the localhost of the guest machine. Instead we can bind the adress to 0.0.0.0 to listen to any adress. 
# Or we can specify the url by using the command docker-machine ip. This will return the ip of the guest machine.