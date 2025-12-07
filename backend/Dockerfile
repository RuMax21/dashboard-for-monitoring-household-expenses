FROM node:20-alpine

RUN apk add --no-cache libc6-compat openssl

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

RUN npx prisma generate

EXPOSE 4000

CMD ["npm", "run", "start:dev"]