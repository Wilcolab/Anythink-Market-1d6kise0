FROM node:16

WORKDIR /app

COPY package*.json ./

RUN npm config set strict-ssl false && npm install

COPY . .

EXPOSE 8001

CMD ["npm", "start"]
