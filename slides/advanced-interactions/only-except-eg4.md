## Examples only / except

The following example will skip the build job if a change is detected in any file in the root directory of the repo with a **.md** extension:

```yaml
build:
  script: npm run build
  except:
    changes:
      - "*.md"
```