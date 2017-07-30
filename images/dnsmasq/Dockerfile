FROM debian:jessie-slim

RUN apt-get update

RUN apt-get install -y dnsmasq
RUN apt-get -y upgrade   

RUN echo "user=root" > /etc/dnsmasq.conf
RUN echo address=/dev/127.0.0.1 >> /etc/dnsmasq.conf

EXPOSE 53 53/udp

ENTRYPOINT ["dnsmasq","-d"]