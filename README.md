```
xhost +
git clone git@github.com:yanoyoshiki/isaac_lab_docker.git
cd isaac_lab_docker/docker
sh build.sh
sh run.sh

# IN DOCKER CONTAINER
cd /isaac-sim
./isaac-sim.sh --allow-root
```
