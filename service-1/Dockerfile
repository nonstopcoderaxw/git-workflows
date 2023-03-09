FROM node:16

# Create app directory
WORKDIR /usr/src/service-1

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN yarn
# If you are building your code for production
# RUN npm ci --only=production

# copy a file to root
COPY ./index.js .

# copy test folder
COPY test /usr/src/service-1/test

EXPOSE 3000
CMD [ "yarn", "start:dev" ]

