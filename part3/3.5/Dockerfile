FROM node:alpine as build-stage

ENV API_URL=http://localhost:8000

WORKDIR /home/node/app/

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build


FROM nginx

COPY --from=build-stage /home/node/app/dist/ /usr/share/nginx/html