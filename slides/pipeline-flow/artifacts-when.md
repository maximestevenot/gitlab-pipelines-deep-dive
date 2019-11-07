## artifacts-when

`artifacts:when` is used to upload artifacts on job failure or despite the failure.

on_success - upload artifacts only when the job succeeds. This is the default.
on_failure - upload artifacts only when the job fails.
always - upload artifacts regardless of the job status.

Examplw:
```yaml
job:
  artifacts:
    when: on_failure
```
