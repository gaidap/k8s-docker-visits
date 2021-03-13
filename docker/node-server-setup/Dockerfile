# Specify a base image. Use sh to start a shell in alpine.
FROM node:alpine

# Create and set folder to place our code. So our project structure does not conflict with the file system.
WORKDIR /usr/src/app

# Install some depenedencies. For our app to work properly we need at least our package.json
COPY ./package.json ./
RUN npm install

# Copy the rest sources to the work directory. This should be at the end of our dockerfile to prevent cache busting.
COPY ./ ./

# Default command
CMD ["npm", "start"]

# If we bind our application to listen to a specific url, like localhost, it will not work. Because the container 
# does not share the localhost of the guest machine. Instead we can bind the adress to 0.0.0.0 to listen to any adress. 
# Or we can specify the url by using the command docker-machine ip. This will return the ip of the guest machine.
# The expose port syntax for running a container os <guestport>:<containerport>. Notice: All arguments placed after the image tag will
# interpreted as arguments or commands for running inside the started container.