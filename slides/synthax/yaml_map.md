### Yaml Maps

You can merge maps in yaml, it is useful to override variables

```yaml
variables:
  APP_NAME: portal-backend
  ENV: staging

deploy:
  script: 
    - echo "Deploy $APP_NAME on $ENV"

deploy:production:
  variables:
    ENV: production
  script: 
    - echo "Deploy $APP_NAME on $ENV"
```

