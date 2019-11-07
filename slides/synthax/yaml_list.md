```yaml
.functions: &functions |

  function print_hello() {
    echo "Hello $1!"
  }

hello-job:
  before_script:
    - 
  script:
    - print_hello "Noida 1"

```