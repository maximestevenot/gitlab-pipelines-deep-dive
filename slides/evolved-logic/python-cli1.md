### The Shell Code

```bash
function create_repository() {
    repos=$(aws ecr describe-repositories)
    export CI_REGISTRY_IMAGE=$(echo $repos | jq -r ".repositories[] | select(.repositoryName == \"$DOCKER_IMAGE_NAME\") | .repositoryUri")

	if [ "$CI_REGISTRY_IMAGE" ]; then
		echo "[INFO] $CI_REGISTRY_IMAGE already exists "
	else
		CI_REGISTRY_IMAGE=$(aws ecr create-repository --repository-name $DOCKER_IMAGE_NAME | jq -r .repository.repositoryUri)
		echo "[INFO] New ecr repository created: $CI_REGISTRY_IMAGE"
	fi
}
```
