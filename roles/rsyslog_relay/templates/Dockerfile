FROM centos:7
MAINTAINER "Outscale IT Team"

RUN     yum -y install rsyslog \
           wget \
           rsyslog-kafka \
           rsyslog-relp

#COPY rsyslog.conf /etc/rsyslog.conf
COPY certs /etc/pki
EXPOSE 20514 20515 9092

CMD /usr/sbin/rsyslogd -n
