FROM node

RUN apt-get update -y && apt-get upgrade -y
RUN cd $(npm root -g)/npm && npm install fs-extra && sed -i -e s/graceful-fs/fs-extra/ -e s/fs.rename/fs.move/ ./lib/utils/rename.js

COPY . /cyclotron-site
WORKDIR /cyclotron-site
#RUN npm install

EXPOSE 8080

ENTRYPOINT ["sh", "./entrypoint.sh"]
# CMD ["gulp", "server"]

# cyclotron site 8080 
