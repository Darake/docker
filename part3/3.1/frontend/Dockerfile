FROM ubuntu:16.04

ENV API_URL=http://localhost:8000

EXPOSE 5000

COPY . /app

RUN apt-get update && apt-get install -y curl && \
    curl -L https://deb.nodesource.com/setup_8.x | bash && \
    apt-get install -y nodejs && \
    cd /app && \
    npm install && \
    apt-get purge -y --auto-remove curl && \
    rm -rf ~/var/lib/apt/lists/* 

WORKDIR /app

CMD [ "npm", "start" ]