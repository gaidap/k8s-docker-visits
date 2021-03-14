# FROM node:alpine
FROM node:alpine as builder
WORKDIR /usr/src/app
COPY package.json .
RUN npm install
COPY . .
RUN npm run build
 
FROM nginx
# COPY --from=0 /app/build /usr/share/nginx/html
COPY --from=builder /usr/src/app/build /usr/share/nginx/html