FROM node:14.17 as node

WORKDIR /app

COPY . .

RUN npm install 

RUN npm run build --prod

#stage 2
FROM nginx:1.19

COPY --from=node /app/dist/angular-app /usr/share/nginx/html




