FROM alpine:3.15.11

RUN apk add --update nodejs npm && apk add ttf-dejavu && apk add xvfb

WORKDIR /root/
COPY ./frontend/ ./

RUN npm install

EXPOSE 3000
ENTRYPOINT ["npm","run","start"]
