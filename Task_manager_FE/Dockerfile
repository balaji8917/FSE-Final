#stage - 1
FROM node:latest as node
LABEL maintainer="balaji8917@gmail.com"
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build --prod

#stage 2
FROM nginx:alpine
COPY --from=node /app/dist/project-manager /usr/share/nginx/html
