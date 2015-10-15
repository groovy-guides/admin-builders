FROM java:openjdk-8-jdk

MAINTAINER duncan@dickinson.name

RUN apt-get update

ENV GROOVY_VERSION 2.4.5
ENV JAVA_HOME /usr/lib/jvm/java-8-openjdk-amd64
ENV GROOVY_HOME /opt/groovy-${GROOVY_VERSION}
ENV PATH $PATH:$GROOVY_HOME/bin

RUN useradd -c "Local Groovy user" -p groovy -m groovy

ADD http://dl.bintray.com/groovy/maven/apache-groovy-binary-${GROOVY_VERSION}.zip /tmp/

#ADD apache-groovy-binary-${GROOVY_VERSION}.zip /tmp/

RUN unzip -d /opt/ /tmp/apache-groovy-binary-${GROOVY_VERSION}.zip \
  && rm /tmp/apache-groovy-binary-${GROOVY_VERSION}.zip

WORKDIR /home/groovy

USER groovy
