```yaml  
image: maven:latest

stages:
  - build
  - test
  - run

build:
  stage: build
  script:
    - mvn compile

test:
  stage: test
  script:
    - mvn test

run:
  stage: run
  script:
    - mvn package
    - mvn exec:java -Dexec.mainClass="com.example.app.App"
```