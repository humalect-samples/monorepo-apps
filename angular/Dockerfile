FROM node:16-alpine AS build
WORKDIR /app
COPY package*.json ./
RUN npm ci
RUN npm install
COPY . .
RUN npm run build
EXPOSE 4200
CMD ["npm", "start"]

# Stage 1: Build the Angular app
# FROM node:18 as build
# WORKDIR /usr/src/app
# COPY package*.json ./
# RUN npm ci
# RUN npm install
# COPY . .
# RUN npm run build

# CMD ["npm", "start"]

# # Stage 2: Serve the Angular app with Nginx
# FROM nginx:alpine

# COPY --from=build /usr/src/app/dist/hello-world-app /usr/share/nginx/html

# EXPOSE 4200

# CMD ["nginx", "-g", "daemon off;"]
