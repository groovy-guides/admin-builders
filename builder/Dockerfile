FROM groovyguides/jdk8

RUN mkdir --parents /usr/src/app
WORKDIR /usr/src/app

COPY envprimer /usr/src/app/

RUN mkdir -p ~/.gradle

RUN ./gradlew build

CMD rm -rf /usr/src/app