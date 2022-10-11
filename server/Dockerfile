FROM node:latest

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# COPY package*.json ./
COPY package.json /usr/src/app/
RUN npm install --silent

# COPY . .
COPY . /usr/src/app

EXPOSE 5000
CMD ["npm", "start"]