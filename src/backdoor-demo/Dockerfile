FROM node:18@sha256:b08b1356559e2e9945f47ded630c9eb9d4e3ca04f111ab20d55652442cf14aee

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install --verbose
# If you are building your code for production
# RUN npm ci --omit=dev

# Bundle app source
COPY . .

EXPOSE 3000
CMD [ "node", "index.js" ]