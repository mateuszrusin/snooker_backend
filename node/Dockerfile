FROM hypriot/rpi-node

#RUN groupadd -r nodejs && useradd -m -r -g nodejs nodejs

#USER nodejs

# Create app directory
# RUN mkdir -p /app
WORKDIR .

#RUN apt-get update  && apt-get install -y npm && apt-get -y autoclean

# Install app dependencies
COPY package.json .
RUN npm install -ddd

# Bundle app source
COPY . .

EXPOSE 3000
CMD [ "npm", "start" ]
