FROM adoptopenjdk/openjdk8-openj9:alpine
VOLUME /tmp
COPY target/dependency/BOOT-INF/lib /app/lib
COPY target/dependency/META-INF /app/META-INF
COPY target/dependency/BOOT-INF/classes /app
ENV JAVA_OPTS=""
ENTRYPOINT ["java","-Xmx128m","-Djava.security.egd=file:/dev/./urandom","-Xms32m","-Xquickstart","-Xshareclasses","-Xscmx128m","-noverify","-cp","app:app/lib/*","hello.Application"]

