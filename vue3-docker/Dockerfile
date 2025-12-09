
FROM node:18-alpine

WORKDIR /app

COPY package*.json ./

# 忽略 SSL 憑證問題
RUN npm config set strict-ssl false

RUN npm install

COPY . .

CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
