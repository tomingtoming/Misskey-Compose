FROM node

RUN npm install node-gyp
ADD src Misskey-API
WORKDIR Misskey-API
RUN npm install
RUN npm run dts
RUN npm run build
ADD config /root/.misskey
CMD npm start
