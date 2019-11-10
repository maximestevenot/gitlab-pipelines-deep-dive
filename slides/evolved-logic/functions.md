## Shell Functions

One way to implement complex logic and factorize code is to use shell functions combined with Yaml Anchors and `before_script`.


```yaml

image: soprabanking/dxp-cicd-tools:1.0.8
stages:
  - Say Hello

.functions: &functions |
  function print_hello() {
    name=${1:?"ERROR"}

    echo "Hello $name!"
    echo "Namaste $name!"
    echo "Bonjour $name!"
  }
  
my-job:
  stage: Say Hello
  before_script:
    - *functions
  script:
    - print_hello "Noida 1"
  tags:
    - dxp-small
```