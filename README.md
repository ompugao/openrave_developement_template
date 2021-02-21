# Prerequiresites
- docker
- docker-compose
- buildkit
- (vscode)

# Usage

```sh
# run only once
# activate buildkit for build cache
# (https://github.com/docker/buildx#setting-buildx-as-default-builder-in-docker-1903)
docker buildx install
cd path/to/openrave_docker_development_template
bash ./set_xauth.sh
git clone https://github.com/rdiankov/openrave
# run vscode

```
