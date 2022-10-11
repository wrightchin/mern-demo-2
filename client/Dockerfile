FROM node:latest

WORKDIR /usr/src/app
COPY package*.json ./

# RUN sudo npm cache clean --force
# RUN sudo npm install --silent
# RUN sudo chown -R 1001:1001 "/root"
# RUN sudo chown -R 1001:1001 "/root/.npm"
# RUN sudo chown 1001:1001 -R /.npm 
# RUN sudo chown -R 1000750000:0 "/.npm"

RUN sudo npm install
RUN sudo chown -R 1000750000:0 "/.npm"
# USER 1001

COPY . .
EXPOSE 3000

CMD ["npm", "start"]