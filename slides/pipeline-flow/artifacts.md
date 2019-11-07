## artifacts

`artifacts` is used to specify a list of files and directories which should be attached to the job when it succeeds, fails, or always.
The artifacts will be sent to GitLab after the job finishes and will be available for download in the GitLab UI.

## artifacts:paths
You can only use paths that are within the local working copy.

Example:
```yaml
artifacts:
  paths:
    - binaries/
    - .config
```