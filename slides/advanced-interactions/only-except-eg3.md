## Examples only / except

The variables keyword is used to define variables expressions. In other words, you can use predefined variables / project / group or environment-scoped variables to define an expression GitLab is going to evaluate in order to decide whether a job should be created or not.

```yaml
deploy:
  script: deploy app
  only:
    refs:
      - branches
    variables:
      - $RELEASE == "staging"
      - $STAGING
```
