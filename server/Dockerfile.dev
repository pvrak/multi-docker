# Use an existing docker image as a Database
FROM node:alpine

#Setup working directory
WORKDIR '/app'

#Copy necessary build files
COPY ./package.json ./

# Download and install a dependency
RUN npm install

COPY . .

#Tell the image what to do when it starts as container
CMD ["npm", "run", "dev"]
