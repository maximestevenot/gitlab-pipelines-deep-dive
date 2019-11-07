### Stages

The specification of stages allows for having flexible multi stage pipelines. The ordering of elements in stages defines the ordering of jobs’ execution:

- Jobs of the same stage are run in parallel.
- Jobs of the next stage are run after the jobs from the previous stage complete successfully.

Every jobs must be part of a stage.

```yaml
stages:
  - Say Hello
  
my-first-job:
  stage: Say Hello
  script: 
    - echo "Hello DxP Noida!"
  tags:
    - dxp-small
```
