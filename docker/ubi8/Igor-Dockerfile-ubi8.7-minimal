FROM quay.io/opsmxpublic/ubi8-jre-11:v1
MAINTAINER sig-platform@spinnaker.io
COPY igor-web/build/install/igor /opt/igor
RUN yum -y install java-11-openjdk-headless.x86_64 wget vim  curl net-tools nettle
RUN yum -y  update
RUN adduser spinnaker
RUN mkdir -p /opt/igor/plugins
RUN chmod -R 777 /opt/igor/plugins/
RUN chown -R spinnaker:spinnaker /opt/
USER spinnaker
CMD ["/opt/igor/bin/igor"]
