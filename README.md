# OpenRAVE + ROS melodic docker environment

![openrave on vscode remote container](https://i.gyazo.com/d856a7f339f7e77fd52a7bab6cda6983.png)
## Prerequiresites
1) docker: https://docs.docker.com/engine/install/ubuntu/
2) docker-compose: https://docs.docker.com/compose/install/
3) nvidia-docker: https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html
4) vscode: Download from Ubuntu Software

## Usage
```sh
# Run only once
git clone https://github.com/ompugao/openrave_docker_development_template
cd path/to/openrave_docker_development_template
touch .devcontainer/.bash_history
git clone https://github.com/ompugao/openrave -b myworkingbranch
git clone https://github.com/personalrobotics/openrave_catkin catkin_ws/personalrobotics/openrave_catkin
git clone https://github.com/ompugao/or_rviz.git catkin_ws/personalrobotics/or_rviz -b hotfix/add_dummy_setbkgndcolor_function
# build dependant docker images
cd .devcontainer && bash build-deps.sh

# Remember to run the following two lines everytime you restart your computer
sudo rm -rf /tmp/.docker.xauth
bash ./set_xauth.sh

# 1. you can use vscode as an IDE.
code .
# and open a container using vscode with remote development plugin
# see: https://code.visualstudio.com/docs/remote/containers-tutorial

# or
# 2. you can use your terminal-based editor such as emacs and vim.
cd .devcontainer/
docker-compose --project-name openrave_docker_development_template -f docker-compose.yml up -d
docker-compose --project-name openrave_docker_development_template -f docker-compose.yml exec -it /bin/bash
```
