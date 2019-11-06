## Examples only / except

In the example below, job will run only for refs that start with `feature/`, whereas all branches will be skipped:

```yaml
job:
  # use regexp
  only:
    - /^feature/.*$/
  # use special keyword
  except:
    - branches
```
