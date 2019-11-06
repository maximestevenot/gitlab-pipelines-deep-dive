## Template Examples

```yaml
include:
  - project: 'my-group/my-project'
    ref: master # Branch
    file: '/templates/.gitlab-ci-template.yml'

  - project: 'my-group/my-project'
    ref: v1.0.0 # Tag
    file: '/templates/.gitlab-ci-template.yml' 

  - project: 'my-group/my-project'
    ref: 787123b47f14b552955ca2786bc9542ae66fee5b # Commit SHA
    file: '/templates/.gitlab-ci-template.yml'
```

```yaml
include:
  - remote: 'https://aws-s3.com/awesome-project/gitlab-ci-template.yml'
```