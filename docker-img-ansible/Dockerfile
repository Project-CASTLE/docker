# docker build -t castle-ansible:0.0.3 .

FROM ubuntu:18.04

# https://docs.ansible.com/ansible/devel/installation_guide/intro_installation.html#latest-releases-via-apt-ubuntu
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y software-properties-common && \
    apt-add-repository --yes --update ppa:ansible/ansible && \
    apt-get install -y ansible && \
    apt-get install -y python-pip

RUN pip install google-auth hvac python-logstash requests

WORKDIR /ansible
ENV ANSIBLE_CONFIG=/ansible/ansible.cfg \
    LOGSTASH_SERVER=logstash \
    LOGSTASH_PORT=5000 \
    VAULT_ADDR=http://vault:8200

COPY ansible /ansible