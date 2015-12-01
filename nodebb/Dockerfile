# Pull base image.
FROM node:4-wheezy
MAINTAINER Erik Dasque <erik@frenchguys.com>

# Install base packages
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install imagemagick build-essential git -y


# Install nodebb
RUN cd /opt && git clone -b v0.9.x https://github.com/NodeBB/NodeBB nodebb
RUN cd /opt/nodebb && head package.json
# Create a mountable volume
VOLUME /opt/nodebb

# Define working directory.
WORKDIR /opt/nodebb

RUN npm install

## my plugins of choice
RUN npm install gm nodebb-plugin-composer-redactor nodebb-plugin-recent-cards
RUN npm install nodebb-plugin-s3-uploads nodebb-plugin-emailer-mandrill
RUN npm install nodebb-plugin-pushbullet
# RUN npm install nodebb-plugin-poll

# Expose ports
EXPOSE 4567

# Define default command.
CMD env ; ./nodebb setup ; ./nodebb upgrade ; ./nodebb start;