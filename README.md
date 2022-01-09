# catkin_purt
PURT mocap base workspace

Build and launch simulation.
```
git submodule update --init --recursive
catkin build
. ./devel/setup.bash
roscd mavros/scripts
sudo ./install_geographiclib_datasets.sh
roslaunch qualisys sim.launch
```
