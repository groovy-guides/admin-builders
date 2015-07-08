#
gradle wrapper

docker build -t groovyguides/builder .

docker run --rm=true -ti groovyguides/builder /bin/bash