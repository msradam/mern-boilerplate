From node:10
RUN mkdir -p /srv/app/server
WORKDIR /srv/app/server

COPY package.json /srv/app/server
COPY yarn.lock /srv/app/server

RUN yarn

COPY . /srv/app/server

CMD ["yarn", "run", "start"]