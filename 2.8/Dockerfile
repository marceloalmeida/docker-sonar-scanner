FROM marceloalmeida/docker-alpine-java:jdk8

MAINTAINER Marcelo Almeida <ms.almeida86@gmail.com>

ENV \
  SONAR_SCANNER_VERSION="2.8" \
  SONAR_SCANNER_OPTS="-Xmx512m"


RUN \
  apk --update --no-cache add curl && \
  cd /opt/ && \
  curl -sOL https://sonarsource.bintray.com/Distribution/sonar-scanner-cli/sonar-scanner-${SONAR_SCANNER_VERSION}.zip && \
  unzip sonar-scanner-${SONAR_SCANNER_VERSION}.zip && \
  rm sonar-scanner-${SONAR_SCANNER_VERSION}.zip && \
  apk del curl

ENV PATH="$PATH:/opt/sonar-scanner-${SONAR_SCANNER_VERSION}/bin"

WORKDIR /root

CMD ["sonar-scanner", "-Dsonar.projectBaseDir=./src"]
