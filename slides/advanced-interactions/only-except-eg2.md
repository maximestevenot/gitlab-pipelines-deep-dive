## More examples

The variables keyword is used to define variables expressions. In other words, you can use predefined variables / project / group or environment-scoped variables to define an expression GitLab is going to evaluate in order to decide whether a job should be created or not.

```yaml
deploy:
  script: deploy app
  only:
    refs:
      - branches
    variables:
      - $RELEASE == "staging"
      - $STAGING
```

The following example will skip the build job if a change is detected in any file in the root directory of the repo with a .md extension:

```yaml
build:
  script: npm run build
  except:
    changes:
      - "*.md"
```