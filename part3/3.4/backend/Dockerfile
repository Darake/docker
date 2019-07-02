FROM node:alpine

USER node

ENV FRONT_URL=http://localhost:5000
ENV NODE_ENV=production

EXPOSE 8000

COPY --chown=node package*.json /home/node/app/

WORKDIR /home/node/app/

RUN npm install

COPY --chown=node . .

CMD [ "node", "index.js" ]