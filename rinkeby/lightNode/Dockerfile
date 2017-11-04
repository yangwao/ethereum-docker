FROM ethereum/client-go:v1.7.2

RUN apk update &&\
    apk add git nodejs bash perl

# RUN cd /root &&\
#    git clone https://github.com/cubedro/eth-net-intelligence-api &&\
#    cd eth-net-intelligence-api &&\
#    npm install &&\
#    npm install -g pm2
#
#ADD app.json /root/eth-net-intelligence-api/app.json

ADD start.sh /root/start.sh
RUN chmod +x /root/start.sh

ENTRYPOINT /root/start.sh
