FROM microsoft/vsts-agent:ubuntu-16.04-docker-17.03.0-ce-standard

ENV SONAR_SCANNER_VERSION=3.0.3.778-linux

RUN wget https://sonarsource.bintray.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-$SONAR_SCANNER_VERSION.zip -O /tmp/sonar-scanner.zip &&\
    unzip /tmp/sonar-scanner.zip -d /usr/share/sonar-scanner &&\
    rm -rf /tmp/sonar-scanner.zip

ENV PATH=$PATH:/usr/share/sonar-scanner/sonar-scanner-$SONAR_SCANNER_VERSION/bin

RUN sonar-scanner -h