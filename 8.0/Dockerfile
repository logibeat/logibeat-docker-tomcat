FROM logibeat/java:latest

ENV CATALINA_HOME /usr/local/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH
RUN mkdir -p "$CATALINA_HOME"
WORKDIR $CATALINA_HOME

ENV TOMCAT_MAJOR 8
ENV TOMCAT_VERSION 8.0.35
ENV TOMCAT_TGZ_URL http://docker-logibeat.oss-cn-shanghai.aliyuncs.com/software/tomcat/$TOMCAT_MAJOR.0/apache-tomcat-$TOMCAT_VERSION.tar.gz

RUN curl -fsSL "$TOMCAT_TGZ_URL" |tar zx --strip-components=1
RUN rm bin/*.bat

EXPOSE 8080
CMD ["$CATALINA_HOME/bin/catalina.sh", "run"]