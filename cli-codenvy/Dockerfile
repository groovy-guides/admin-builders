FROM groovyguides/jdk8-codenvy
RUN mkdir /home/user/app
WORKDIR /home/user/app
ADD $app$ /home/user/$app$
RUN unzip -q /home/user/$app$ -d /home/user/app && \
    rm /home/user/$app$ && \
    chmod +x gradlew

# expected to have all dependencies in lib directory and one single jar file application.jar in 'root' directory of archive.
CMD ./gradlew run