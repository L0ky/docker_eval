FROM node:12.18.3
WORKDIR /app
COPY app.js .
RUN npm install amqplib -y
CMD ["node", "app.js"]