FROM node:lts-alpine as build-stage
WORKDIR /app
COPY ./package*.json ./
RUN npm install
COPY ./ ./
RUN npm run build

FROM nginx:stable-alpine as production-stage
LABEL maintainer="Patrick Lima <patrickm.lima1@gmail.com"
ENV NODE_ENV=production
COPY --from=build-stage /app/dist /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
