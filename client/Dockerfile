FROM node:alpine as builder
#Setup working directory
WORKDIR '/app'
#Copy necessary build files
COPY ./package.json ./
# Download and install a dependency
RUN npm install
COPY . .
RUN npm run build

FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /app/build /usr/share/nginx/html
