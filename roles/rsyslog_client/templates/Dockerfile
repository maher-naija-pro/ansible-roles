FROM rockylinux/rockylinux:8
MAINTAINER "Outscale IT Team"

RUN     yum -y install rsyslog \
           wget \
           rsyslog-relp

EXPOSE 20514 20515

CMD /usr/sbin/rsyslogd -n
