FROM node:12.22.1-alpine3.11
RUN apk add --no-cache python g++ make
WORKDIR /app
COPY . .
RUN apk --no-cache --virtual build-dependencies add \
        python \
        make \
        g++
RUN yarn install --production

CMD ["node", "/app/src/index.js"]
