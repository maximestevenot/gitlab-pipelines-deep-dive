## Before Script

`before_script` is used to run commands previously those of the main script. It is very useful to factorize code.

```yaml
stages:
  - Test

.angular:
  image: trion/ng-cli-karma:latest
  stage: Test
  before_script:
    - if ! [ -d node_modules ] ; then npm install ; fi
  cache:
    key: $CI_COMMIT_REF_SLUG
    paths:
      - node_modules/

lint:
  extends: .angular
  script:
    - npm run lint

unit-tests:
  extends: .angular
  script:
    - ng test --watch=false --code-coverage
  coverage: '/^Statements\s*:\s*([^%]+)/'
```