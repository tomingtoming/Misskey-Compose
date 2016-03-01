FROM node

RUN npm install node-gyp
ADD src Misskey-Web
WORKDIR Misskey-Web
RUN npm install
RUN npm run dtsm
RUN GIT_DIR=/Misskey-Web ./node_modules/.bin/bower install --allow-root
RUN npm run build
ADD config /root/.misskey
CMD npm start
