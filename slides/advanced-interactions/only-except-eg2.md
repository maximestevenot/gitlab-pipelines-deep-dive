## Examples only / except

In this example, job will run only for refs that are tagged, or if a build is explicitly requested via an API trigger or a Pipeline Schedule:

```yaml
job:
  # use special keywords
  only:
    - tags
    - triggers
    - schedules
```