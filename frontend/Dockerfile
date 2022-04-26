ARG NODE_VERSION
ARG NPM_VERSION
ARG NGINX_VERSION

FROM node:${NODE_VERSION} as builder

WORKDIR /app

COPY package.json .
COPY yarn.lock .
RUN yarn install --immutable --inline-builds

COPY . .

RUN yarn build --configuration production

FROM nginx:${NGINX_VERSION}

COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /app/dist/app /usr/share/nginx/html
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
