FROM node:16

WORKDIR /app

COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

COPY package.json .
COPY package-lock.json .

RUN npm config set unsafe-perm true
RUN npm i --silent --force

COPY . .

RUN chown -R node:node /app/node_modules

USER node

ENTRYPOINT [ "/entrypoint.sh" ]

CMD ["npm", "run", "dev"]
