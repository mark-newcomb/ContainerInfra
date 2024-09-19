FROM almalinux/9-base
COPY . /app

RUN yum clean all
RUN yum update -y

RUN yum install -y python3
RUN yum install -y pip
RUN python3 -m pip install --upgrade pip
RUN pip install ansible

RUN yum install -y sshpass
RUN yum install -y passwd
RUN echo 'ansibleinfra' | passwd --stdin root
RUN yum install -y net-tools
RUN yum install -y openssh
RUN yum install -y openssh-server
RUN yum install -y openssh-clients
RUN echo 'PermitRootLogin yes' >> /etc/ssh/sshd_config

ENTRYPOINT ["/sbin/init"]
