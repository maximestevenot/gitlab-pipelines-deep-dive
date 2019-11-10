## Write business logic in python

CICD Team have decided to write more complex logic in Python in order to perform unit tests and apply design patterns.

```yaml
docker-push:
  image: soprabanking/dxp-cicd-tools
  services:
    - docker:18-dind
  before_script:
    - $(aws ecr get-login --no-include-email)
    - pip install dxp-ci --extra-index-url "$DXP_CI_PY_URL"
  script:
    - dxp-ci ecr create $IMAGE_NAME
    - docker push $AWS_REGISTRY_URL/$IMAGE_NAME:$IMAGE_VERSION
```

DxP CICD [CLI](https://innersource.soprasteria.com/dxp/dxp-cicd/gitlab-ci-toolset/cicd.python/dxp_ci) and [Common Library](https://innersource.soprasteria.com/dxp/dxp-cicd/gitlab-ci-toolset/cicd.python/dxp_commons)
