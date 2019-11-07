### Tags

Tags allow you to select the runner where you want to execute your job.  
Three (`dxp-small`,`dxp-large` and `dxp` == `dxp-medium`) are availables in DxP and you **must** pick one of them.

```yaml
my-first-job:
  script: 
    - echo "Hello DxP Noida!"
  tags:
    - dxp-small
```
