# catkin_purt
PURT mocap base workspace

This repository locks down the mavlink and mavros
versions for a specific version of PX4. By building
from source within the workspace, this will prevent ubuntu mavros
/mavlink package updates from breaking the build due to incompatible
mavlink versions.

This is also a catkin only build workspace, meaning you do not
need to call make manually on the px4 repository and then export 
the paths.

Build and launch simulation.
```
git submodule update --init --recursive
catkin build
. ./devel/setup.bash
roscd mavros/scripts
sudo ./install_geographiclib_datasets.sh
roslaunch qualisys sim.launch
```
