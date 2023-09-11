FROM rockylinux/rockylinux:8
MAINTAINER "Outscale IT Team"

RUN yum -y install postfix; yum -y install mailx; yum clean all; systemctl enable postfix
COPY main.cf master.cf /etc/postfix/
COPY {{ postfix_smtpd_tls_key_file }} {{ postfix_smtpd_tls_cert_file }}  /etc/ssl/certs/
EXPOSE 587

CMD [ "/usr/sbin/init" ]