FROM node:16.13.2 as build

WORKDIR /app
COPY package*.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx:1.18
COPY ./nginx/nginx.conf /etc/nginx/nginx.conf
COPY --from=build /app/public /usr/share/nginx/html