FROM node:16-alpine

RUN apk update

RUN apk --update add tzdata && \ 
    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \ 
    echo "Asia/Tokyo" >  /etc/timezone

RUN apk add git

RUN git clone -b ver_2 https://github.com/eALPS/SHINtube.git

WORKDIR /SHINtube

RUN npm install

CMD ["npm","start"] 