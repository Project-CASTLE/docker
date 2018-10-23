FROM elastic/filebeat:6.4.0

COPY config/filebeat.yml /usr/share/filebeat/filebeat.yml
USER root
RUN chown root:filebeat /usr/share/filebeat/filebeat.yml
#USER filebeatdt