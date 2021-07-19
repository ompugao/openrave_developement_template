# OpenRAVE + ROS melodic docker environment

![openrave on vscode remote container](https://i.gyazo.com/d856a7f339f7e77fd52a7bab6cda6983.png)
## Prerequiresites
1) docker: https://docs.docker.com/engine/install/ubuntu/
2) docker-compose: https://docs.docker.com/compose/install/
3) nvidia-docker: https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html
4) vscode: Download from Ubuntu Software

## Usage

```sh
# run only once
1) git clone https://github.com/ompugao/openrave_docker_development_template
2) cd path/to/openrave_docker_development_template
3) touch .devcontainer/.bash_history
4) git clone https://github.com/ompugao/openrave.git
5) git clone https://github.com/personalrobotics/openrave_catkin catkin_ws/personalrobotics/openrave_catkin
6) cd catkin_ws/personalrobotics && git clone https://github.com/ompugao/or_rviz.git
7) cd .. x2
8) cd openrave && git checkout myworkingbranch && cd ../catkin_ws/personalrobotics/or_rviz && git checkout hotfix/add_dummy_setbkgndcolor_function
9) cd .. x3
10) sudo rm -rf /tmp/.docker.xauth
11) bash ./set_xauth.sh
(Remember to run 10 & 11 everytime you restart your computer!)

Open vscode to continue:
Open container using vscode: https://code.visualstudio.com/docs/remote/containers-tutorial
2) Open folder to containers
3) Start a new terminal.
3) cd .devcontainer/ && bash build-deps.sh && docker-compose up

```
