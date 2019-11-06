## Examples only/except

In the example below, job will run only for refs that start with feature/, whereas all branches will be skipped:

```yaml
job:
  # use regexp
  only:
    - /^feature/.*$/
  # use special keyword
  except:
    - branches
```

In this example, job will run only for refs that are tagged, or if a build is explicitly requested via an API trigger or a Pipeline Schedule:

```yaml
job:
  # use special keywords
  only:
    - tags
    - triggers
    - schedules
```