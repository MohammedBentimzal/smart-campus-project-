FROM node:22-slim 

WORKDIR /frontend 

COPY /package*.json ./

COPY . .

RUN npm install 

CMD [ "npm","run","dev" ]