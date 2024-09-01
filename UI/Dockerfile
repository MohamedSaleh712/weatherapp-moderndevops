FROM node:alpine

WORKDIR /ui
COPY ./package*.json/ .
RUN npm install
COPY . .
EXPOSE 3000

ENTRYPOINT [ "node" ]
CMD [ "app.js" ]