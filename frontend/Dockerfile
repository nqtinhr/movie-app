# Stage 1
FROM node:alpine3.18 as build-stage

WORKDIR /frontend

COPY package*.json .

RUN npm install

COPY . .

RUN npm run build

# Stage 2
FROM nginx:alpine3.18

COPY --from=build-stage /frontend/build /usr/share/nginx/html

CMD nginx -g 'daemon off;'