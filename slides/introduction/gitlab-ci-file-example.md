## Example of **.gitlab-ci.yml** file:

```yaml
stages:
  - hello

hello-job:
  stage: hello
  script:
    - echo "Hello World!"
```