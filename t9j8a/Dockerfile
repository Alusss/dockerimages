FROM alpine
MAINTAINER Alusss
ENV REFRESHED_AT 2020-04-28

WORKDIR /usr
RUN mkdir jdk
RUN mkdir tomcat

ADD jdk1.8.0_231 /usr/jdk/
ADD apache-tomcat-9.0.34 /usr/tomcat/

ENV JAVA_HOME=/usr/jdk
ENV JRE_HOME=$JAVA_HOME/jre
ENV CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar:$JRE_HOME/lib:$CLASSPATH
ENV PATH=/sbin:$JAVA_HOME/bin:$PATH

EXPOSE 8080

ENTRYPOINT ["/usr/tomcat/bin/catalina.sh","run"]
