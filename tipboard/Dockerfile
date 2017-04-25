FROM ubuntu:16.04

RUN apt-get update -q && \
    apt-get install -qqy python-dev python-pip supervisor && \
    apt-get clean && \
    pip install tipboard && \
    mkdir /root/logs /root/.tipboard

ADD /supervisord.conf /etc/supervisor/supervisord.conf
ADD /files /root/.tipboard

EXPOSE 7272

CMD ["/usr/bin/supervisord", "-j", "/root/supervisord.pid"]
