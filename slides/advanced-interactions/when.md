## When keyword
`when` is used to implement jobs that are run in case of failure or despite the failure. `when` can be set to one of the following values:

1. `on_success` - execute job only when all jobs from prior stages succeed (or are considered succeeding because they are marked allow_failure). This is the default.
2. `on_failure` - execute job only when at least one job from prior stages fails.
3. `always` - execute job regardless of the status of jobs from prior stages.
4. `manual` - execute job manually (added in GitLab 8.10). Read about manual actions belo

```yaml
deploy_job:
  stage: deploy
  script:
    - make deploy
  when: manual
```  
