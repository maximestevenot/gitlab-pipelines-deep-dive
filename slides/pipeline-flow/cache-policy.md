### cache:policy

The default behaviour of a caching job is to download the files at the start of execution, and to re-upload them at the end.
This allows any changes made by the job to be persisted for future runs, and is known as the `pull-push` cache policy.
You can skip the upload step by setting `policy: pull` in the job specification.

```yaml
rspec:
  stage: test
  cache:
    key: gems
    paths:
      - vendor/bundle
    policy: pull
  script:
    - bundle install
```