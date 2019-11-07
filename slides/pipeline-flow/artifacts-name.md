### artifacts:name

The `name` directive allows you to define the name of the created artifacts archive. That way, you can have a unique name for every archive which could be useful
when you’d like to download the archive from GitLab.
The `artifacts:name` variable can make use of any of the predefined variables. The default name is artifacts, which becomes artifacts.zip when downloaded.

```yaml
job:
  artifacts:
    name: "$CI_JOB_NAME"
    paths:
      - binaries/
```
