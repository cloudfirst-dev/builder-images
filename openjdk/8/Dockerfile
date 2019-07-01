FROM centos:7

USER root

RUN yum install -y \
       java-1.8.0-openjdk-1.8.0.212.b04-0.el7_6 \ 
       java-1.8.0-openjdk-devel-1.8.0.212.b04-0.el7_6 \ 
       maven \
    && echo "securerandom.source=file:/dev/urandom" >> /usr/lib/jvm/jre/lib/security/java.security \
    && yum clean all

RUN groupadd -r openjdk -g 1001 \
  && useradd -u 1001 -r -g openjdk -m -d /opt/jboss -s /sbin/nologin openjdk

USER openjdk
