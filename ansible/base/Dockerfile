# BASE image - used as a starting point by MASTER and HOST images
FROM ansible/centos7-ansible:stable

# install base tools
RUN yum install -y openssh-server vim man net-tools \
    iputils python3

# generate host keys
RUN /usr/bin/ssh-keygen -A

# ensure that required directories are created
RUN mkdir /var/run/sshd
RUN mkdir /root/.ssh
