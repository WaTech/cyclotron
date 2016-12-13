FROM node
RUN apt-get update -y && apt-get upgrade -y

COPY . /cyclotron-svc
WORKDIR /cyclotron-svc
RUN npm install
COPY config/sample.config.js config/config.js

EXPOSE 8077

CMD ["node", "app.js"]

# cyclotron REST API 8077