# Docker Sonar Scanner
====================

Common library used by many Scanners (SQ Scanner, SQ Scanner for Maven, SQ Scanner for Gradle, SQ Scanner for Ant, ...). Used to programmatically run SQ analysis.

[![Build Status](https://travis-ci.org/marcelosousaalmeida/docker-sonar-scanner.svg?branch=master)](https://travis-ci.org/marcelosousaalmeida/docker-sonar-scanner)

# Usage:
```sh
docker run -it --rm -v $PWD:/root/src marceloalmeida/docker-sonar-scanner:latest
```

# Usage (parsing Sonar parameters):
```sh
docker run -it --rm -v $PWD:/root/src marceloalmeida/docker-sonar-scanner:latest sonar-scanner -Dsonar.projectBaseDir=/root/src -Dsonar.host.url=https://sonarqube.yourcompany.com 
```

# Useful links
* [Sonarqube Documentation - Analysis Parameters](https://docs.sonarqube.org/display/SONAR/Analysis+Parameters)
* [Sonarqube Documentation - Local and Branch Analysis](https://docs.sonarqube.org/display/SONAR/Local+and+Branch+Analysis)
* [Sonarqube Documentation - GitHub Plugin](https://docs.sonarqube.org/display/PLUG/GitHub+Plugin)
