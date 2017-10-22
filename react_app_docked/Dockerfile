# pulls in the latest node image
# getting latest from the node docker image
FROM node:latest

MAINTAINER Wes Duff

ENV         NODE_ENV=test
ENV         PORT=3000

#copy entier app 
COPY        . /var/www
#need this to know where our package.json is located
WORKDIR     /var/www

RUN         npm install 

# this is the default for create-react-app ... so we choose 3000 for the port
#read this from the env variables
EXPOSE $PORT

# This is treated as a JSON array under the covers, so we need double quotes
ENTRYPOINT ["npm", "start"]

#need to copy source code into this image
