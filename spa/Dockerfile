FROM node:15.9
WORKDIR /usr/src/frontend
COPY . .
RUN echo "VUE_APP_API_ENDPOINT=\"http://127.0.0.1:4001/api\"" > .env.production
RUN npm config set user 0
RUN npm config set unsafe-perm true
RUN npm install && npm install -g @vue/cli
RUN npm run build

FROM nginx:1.18
COPY --from=0 /usr/src/frontend/dist /usr/share/nginx/html
EXPOSE 80