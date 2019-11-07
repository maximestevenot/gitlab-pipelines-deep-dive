### Images

You must specify a Docker image **with its version** to use for the job. Image can be global and be overriden in each job.

```yaml
image: soprabanking/dxp-cicd-tools:1.0.8

stages:
  - Say Hello
  
my-first-job:
  stage: Say Hello
  image: busybox:1.31
  script: 
    - echo "Hello DxP Noida!"
  tags:
    - dxp-small
```
