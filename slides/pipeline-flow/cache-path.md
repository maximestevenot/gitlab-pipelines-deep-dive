### cache:paths
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