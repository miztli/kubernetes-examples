FROM openjdk:8u181-alpine3.8

ARG WORKDIR="/app"
ARG PORT=8080

RUN mkdir ${WORKDIR}

COPY ./build/libs/properties-samples-0.0.1-SNAPSHOT.jar ${WORKDIR}

WORKDIR ${WORKDIR}

EXPOSE ${PORT}

CMD [ "java", "-jar", "properties-samples-0.0.1-SNAPSHOT.jar" ]