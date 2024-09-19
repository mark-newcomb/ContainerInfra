FROM almalinux/8-base

RUN yum clean all
RUN yum update -y
RUN yum install -y sshpass
RUN yum install -y passwd
RUN echo 'ansibleinfra' | passwd --stdin root
RUN yum install -y net-tools
RUN yum install -y openssh
RUN yum install -y openssh-server
RUN yum install -y openssh-clients
RUN echo 'PermitRootLogin yes' >> /etc/ssh/sshd_config

ENTRYPOINT ["/sbin/init"]