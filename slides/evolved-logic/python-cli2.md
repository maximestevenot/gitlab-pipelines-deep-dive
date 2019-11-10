### The Python Code

```python
def create_repository(repository_name):
    ecr = boto3.client('ecr')
    try:
        response = ecr.create_repository(repositoryName=repository_name)
        env.LOGGER.debug(response)
    except ecr.exceptions.RepositoryAlreadyExistsException:
        env.LOGGER.info(
            "Repository {repo} already exists".format(repo=repository_name))
    except ClientError as e:
        raise JobAbortException(e)

```
