FROM node:12.14.0-alpine3.11 as base

RUN apk add --no-cache bash git

RUN touch /home/node/.bashrc | echo "PS1='\w\$ '" >> /home/node/.bashrc

RUN npm config set cache /home/node/app/.npm-cache --global

RUN npm i -g @nestjs/cli

USER node

WORKDIR /home/node/app

EXPOSE 3000

CMD /bin/sh

#FROM base as prod
#
#COPY app /home/node/app
#
#CMD npm run start