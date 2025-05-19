FROM node:18

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

RUN npm install -g @nestjs/cli

RUN npx prisma generate
RUN npx prisma db push

EXPOSE 3000

CMD ["npm", "run", "start:dev"]
