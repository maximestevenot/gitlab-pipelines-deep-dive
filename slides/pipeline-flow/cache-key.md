## cache:key

Since `cache` is shared between jobs, if you’re using different paths for different jobs, you should also set a different cache:key otherwise cache content can be overwritten
The `key` directive allows you to have a single cache for all jobs, cache per-job, cache per-branch or any other way that fits your workflow.
The `cache:key`variable can use any of the predefined variables, and the default key, if not set, is just literal default which means everything is shared between each pipelines

```yaml
cache:
  key: "$CI_COMMIT_REF_SLUG"
  paths:
    - binaries/
```