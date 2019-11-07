## dependencies

By default, all artifacts from all previous stages are passed, but you can use the `dependencies` parameter to define a limited list of jobs (or no jobs) to fetch artifacts from.
If the artifacts of the job that is set as a dependency have been expired or erased, then the dependent job will fail.

Example:
```yaml
build:linux:
  stage: build
  script: make build:linux
  artifacts:
    paths:
      - binaries/

test:linux:
  stage: test
  script: make test:linux
  dependencies:
    - build:linux
```
