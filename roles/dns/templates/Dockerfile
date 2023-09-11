FROM rockylinux/rockylinux:8
MAINTAINER "Outscale IT Team"

RUN yum update -y \
     && yum install -y bind bind-utils openssl \
     && yum clean all \
     && yum clean metadata
COPY etc/named.conf /etc/
COPY var/named/forward.outscale.cloud var/named/forward.outscale var/named/reverse.outscale /var/named/
RUN rndc-confgen -a; chown root:named /etc/rndc.key ; chmod 640 /etc/rndc.key

EXPOSE 53/udp 53/tcp 10000/tcp
ENTRYPOINT /usr/sbin/named -u named -c /etc/named.conf -f