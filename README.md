# docker-sonarqube-scanner

Runs sonar-scanner in a docker container so you don't have to pollute your system with Java or other dependencies.

To pull and run
```
docker run -ti -v $(pwd):/root/src gleyvaglez/sonarqube-scanner
```

# Example Project Config

You need a sonar-project.properties in the root of your project file heres
a template for java
```
# Required metadata
sonar.host.url=http://sonarqube.example.com
sonar.projectKey=key
sonar.projectName=Name
sonar.login=<sonar token>
sonar.projectVersion=1.0

# Comma-separated paths to directories with sources (required)
sonar.sources=<SRC>

# Language
sonar.language=java
sonar.java.binaries=**/target/classes
sonar.java.source=1.8

# Encoding of the source files
sonar.sourceEncoding=UTF-8
```

Many other options you can see in https://www.devopsschool.com/tutorial/sonarqube/sonarqube-properties.html

# Update

For update Sonarqube Scanner CLI Docker image using Docker Hub modify scanner-version file.
Correct value can be found here: https://docs.sonarqube.org/display/SCAN/Analyzing+with+SonarQube+Scanner
