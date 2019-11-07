### Yaml Maps

You can merge maps in yaml, it is useful to override variables

```yaml
image: soprabanking/dxp-cicd-tools:1.0.8
stages:
  - Deployment

variables:
  APP_NAME: portal-backend
  ENV: staging

deploy:
  stage: Deployment
  script: 
    - echo "Deploy $APP_NAME on $ENV"
  tags:
    - dxp-small
    
deploy:production:
  stage: Deployment
  variables:
    ENV: production
  script: 
    - echo "Deploy $APP_NAME on $ENV"
  tags:
    - dxp-small
```

