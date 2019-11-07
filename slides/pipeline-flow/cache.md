## cache

'cache' is used to specify a list of files and directories which should be cached between jobs. You can only use paths that are within the local working copy.
If 'cache' is defined outside the scope of jobs, it means it is set globally and all jobs will use that definition

## cache:paths
Use the `paths` directive to choose which files or directories will be cached. You can only specify paths within your $CI_PROJECT_DIR

Example:
Cache all files in binaries that end in .apk and the .config file:

```yaml
job:
  script:
    - apk-build
  cache:
    paths:
      - binaries/*.apk
      - .config
```