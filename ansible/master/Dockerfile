# MASTER image - used to create the master container to manage hosts

# use builded ansible_base (defined in ../base/Dockerfile) as a starting point
FROM ansible_base:latest
ENV ANSIBLE_CONFIG=/var/ans/ansible.cfg

# copy content of ansible directory from local disk to file system inside Docker image
COPY ansible /var/ans/

# change working directory
WORKDIR /var/ans

# generate RSA key pair to allow master to communicate with managed nodes
RUN ssh-keygen -t rsa -C "master key" -f master_key

