### Yaml Anchors

You can use YAML anchors with scripts, which makes it possible to include a predefined list of commands in multiple jobs. You can't merge lists in yaml.

```yaml
image: soprabanking/dxp-cicd-tools:1.0.8
stages:
  - Say Hello

.functions: &functions |
  function print_hello() {
    echo "Hello $1!"
  }
  
my-second-job:
  stage: Say Hello
  before_script:
    - *functions
  script:
    - print_hello "Noida 1"
  tags:
    - dxp-small
```