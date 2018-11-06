# docker build -t castle-ansible:0.0.2 .

FROM ubuntu:18.04

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y ansible && \
    apt-get install -y python-pip

RUN pip install python-logstash hvac

WORKDIR /ansible
ENV ANSIBLE_CONFIG=/ansible/ansible.cfg \
    LOGSTASH_SERVER=logstash \
    LOGSTASH_PORT=5000 \
    VAULT_ADDR=http://vault:8200

COPY ansible /ansible