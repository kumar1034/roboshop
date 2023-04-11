FROM node:14

EXPOSE 8080

WORKDIR /opt/server

#RUN addgroup roboshop && adduser --system cartuser && chgrp roboshop cartuser 
RUN addgroup roboshop && adduser cartuser && chgrp roboshop /opt/server && chmod g+w /opt/server

RUN chown -R cartuser:roboshop /opt/server/

USER cartuser

COPY package.json /opt/server/

RUN npm install

COPY server.js /opt/server/

CMD ["node", "server.js"]

