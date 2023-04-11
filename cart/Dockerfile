FROM node:14

EXPOSE 8080

WORKDIR /opt/server

RUN addgroup roboshop && adduser cartuser -G roboshop

RUN chown -R cartuser:roboshop /opt/server/

COPY package.json /opt/server/

RUN npm install

COPY server.js /opt/server/

CMD ["node", "server.js"]

