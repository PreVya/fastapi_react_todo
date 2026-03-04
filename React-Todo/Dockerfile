FROM node:16-alpine

RUN addgroup -S appgroup && adduser -m -S appuser -G appgroup

WORKDIR /app

RUN chown -R appuser:appgroup /app

USER appuser

COPY react-todo/package.json .

RUN yarn install 

COPY . .

EXPOSE 3000

CMD ["yarn", "start"]