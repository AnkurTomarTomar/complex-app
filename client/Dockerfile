FROM node:15.11.0-alpine

WORKDIR '/app'

COPY ./package.json .
RUN npm install
COPY . .

FROM nginx:latest
EXPOSE 80
COPY --from=0 /app/build /usr/share/nginx/html

# COPY --from=builder /app/build /var/www/html
