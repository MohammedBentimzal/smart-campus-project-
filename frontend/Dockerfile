FROM node:22-slim 

WORKDIR /frontend 

COPY package*.json ./

RUN npm ci
#npm ci:clean install,package.json and package lock needs to have the same dependencies 
#while npm install can update package lock but npmci return an error   
COPY . .
#why we use the first copy if we'll copoy everything anyway 
#because docker uses caching if there's no change in package.json it'll pass directly to copy the code changes 

EXPOSE 3000

CMD ["npm", "run", "dev", "--", "--hostname", "0.0.0.0"]

#react is a js library it makes u devide interface into reusable component 
#while next.js :is a react framework with additional features like:
    #pages routing #backend api endpoints #