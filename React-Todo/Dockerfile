FROM node:16-alpine

RUN addgroup -S appgroup && adduser -S appuser -G appgroup

WORKDIR /app

RUN chown -R appuser:appgroup /app

USER appuser

COPY package.json yarn.lock ./

RUN yarn install 

COPY . .

EXPOSE 3000

CMD ["yarn", "start"]