FROM resin/rpi-raspbian:jessie

RUN groupadd -r mongodb && useradd -r -g mongodb mongodb \
  && mkdir -p /data/db && rm -rf /data/db/mongod.lock

WORKDIR /usr/local/bin

COPY mongod .

EXPOSE 27017

CMD ["mongod"]
