# Stage 1: Build the Angular app
FROM node:18 AS build

WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install
COPY . .
RUN npm run build --prod

# Stage 2: Serve the app using Nginx
FROM nginx:alpine
COPY --from=build /app/dist/my-angular-app /usr/share/nginx/html

# Optional: Replace default nginx config (optional)
COPY nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
