FROM node:15.9
WORKDIR /usr/src/frontend
COPY . .
RUN npm install -d && npm install -d -g @vue/cli
RUN npm run build

FROM nginx:1.18
COPY --from=0 /usr/src/frontend/dist /usr/share/nginx/html
EXPOSE 80