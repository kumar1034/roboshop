FROM node:14-alphine

EXPOSE 8080

WORKDIR /opt/server

RUN addgroup roboshop && adduser --system cartuser && usermod -aG roboshop cartuser 

RUN chown -R cartuser:roboshop /opt/server/

USER cartuser

COPY package.json /opt/server/

RUN npm install

COPY server.js /opt/server/

CMD ["node", "server.js"]

