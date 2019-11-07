## Gitlab Extends

Thanks to `extends` keyword we can factorize code. The previous example of yaml map becomes:

```yaml
variables:
  APP_NAME: portal-backend
  ENV: staging

deploy:
  script: 
    - echo "Deploy $APP_NAME on $ENV"

deploy:production:
  extends: deploy
  variables:
    ENV: production
```

