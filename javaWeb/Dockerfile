FROM ubuntu:14.04
LABEL description="the image only has jdk and tomcat"
#RUN apt-get update
ADD jdk-8u141-linux-x64.tar.gz /usr/local/java
ENV JAVA_HOME /usr/local/java/jdk1.8.0_141
ENV PATH $JAVA_HOME/bin:$PATH
ENV CLASSPATH .:$JAVA_HOME/lib
ADD apache-tomcat-8.5.16.tar /usr/local/tomcat/
RUN chmod +x /usr/local/tomcat/apache-tomcat-8.5.16/bin/*.sh
EXPOSE 58080
ENTRYPOINT /usr/local/tomcat/apache-tomcat-8.5.16/bin/catalina.sh run && /bin/bash 
