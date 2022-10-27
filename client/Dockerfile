# FROM node:16-alpine

# RUN mkdir -p /usr/src/app &&\
#     chown -R node:node /usr/src/app

# WORKDIR /usr/src/app

# RUN chgrp -R 0 /usr/src/app &&\
#  chmod -R g+rwX /usr/src/app

# COPY package*.json ./

# # RUN sudo npm install --silent
# # RUN chown -R 1001:0 /usr/src/app
# # RUN sudo chown -R 1001:1001 "/root/.npm"
# # RUN sudo chown 1001:1001 -R /.npm 
# # RUN sudo chown -R 1000750010:0 "/.npm"
# # RUN chown -R 1001:0 /.npm
# # RUN chown -R 1001:0 "/npm"
# USER 1001
# RUN npm install

# # RUN sudo chown -R 1000750010:0 "/.npm"
# # USER 1001
# COPY --chown=node:node . /usr/src/app

# # COPY . .
# EXPOSE 3000

# CMD ["npm", "start"]

FROM node:14-alpine

RUN mkdir -p /usr/src/app &&\
 chown -R node:node /usr/src/app 

WORKDIR /usr/src/app

RUN chgrp -R 0 /usr/src/app &&\
 chmod -R g+rwX /usr/src/app

COPY package*.json /usr/src/app

RUN npm install
# RUN mkdir /usr/src/app/node_modules/.cache &&\
#     mkdir /usr/src/app/node_modules/.cache/.eslintcache &&\
#     chmod -R 775 /usr/src/app/node_modules/.cache/.eslintcache

# COPY --chown=node:node . /usr/src/app
COPY . .

RUN chown -R node:node /usr/src/app/node_modules &&\
    chmod 777 /usr/src/app/node_modules

USER node

EXPOSE 3000
CMD ["npm", "start"]