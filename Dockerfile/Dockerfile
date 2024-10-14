FROM node:18-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

RUN adduser -D appuser

RUN chown -R appuser:appuser /app

COPY . .

EXPOSE 8080

USER appuser

CMD ["npm", "start"]
