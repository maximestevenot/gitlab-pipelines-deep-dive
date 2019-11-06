## Example trigger keyword

It is possible to configure a branch name that GitLab will use to create a downstream pipeline with:

```yaml
rspec:
  stage: test
  script: echo "trigger"

staging:
  stage: deploy
  trigger:
    project: my/deployment
    branch: stable
```