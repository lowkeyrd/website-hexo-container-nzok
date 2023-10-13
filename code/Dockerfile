FROM node:16.15

WORKDIR /workspace

RUN wget https://download.java.net/java/GA/jdk21/fd2272bbf8e04c3dbaee13770090416c/35/GPL/openjdk-21_linux-x64_bin.tar.gz && tar zxvf openjdk-21_linux-x64_bin.tar.gz

COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

EXPOSE 9000
ENTRYPOINT [ "node", "index.js" ]