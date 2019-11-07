## Gitlab Extends

Thanks to `extends` keyword we can factorize code. The previous example of yaml map becomes:

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
  extends: deploy
  variables:
    ENV: production
```

