## *Bridging between ROS 1 and ROS 2* ✨

### *1. Install ros1-bridge package using the command:* 🌟

```
sudo apt-get ros-foxy-ros1-bridge
```

### *2. Source ROS 1 and run any file:* 🌟

*terminal 1: running roscore command*
```
source /opt/ros/noetic/setup.bash
roscore
```
![Screenshot_1](https://github.com/le9na/using-ros-bridge/assets/90223879/c6baf789-ca08-4bf7-91ea-09f0e3fc717a)

*terminal 2: checking topics and running talker*
```
rostopic list

rosrun tospy_tutorials talker
```

![Screenshot_2](https://github.com/le9na/using-ros-bridge/assets/90223879/9c423c9a-4713-42c9-9aba-d37156814f4c)

*checking topics again after running talker: topic chatter is now in the list!*

![Screenshot_3](https://github.com/le9na/using-ros-bridge/assets/90223879/e82d4e52-57a8-43d6-ace7-2dc97b440cd2)

------------------------------------------------------------------------------------------------

### *3. Source ROS 2 and run the topic list command:* 🌟

```
source /opt/ros/foxy/setup.bash

ros2 topic list
```

![Screenshot_4](https://github.com/le9na/using-ros-bridge/assets/90223879/efc9b85b-1f5c-43c7-af2c-1bf0eb87732d)

------------------------------------------------------------------------------------------------

### *4. Source ROS 2 in another terminal and run the bridge command:* 🌟

```
source /opt/ros/foxy/setup.bash

ros2 run ros1_bridge dynamic_bridge --bridge-all-topics
```

![Screenshot_5](https://github.com/le9na/using-ros-bridge/assets/90223879/f08ab453-f53b-48a7-b629-202ec49d8c06)

------------------------------------------------------------------------------------------------

### *5. Back in the first ROS 2 terminal, run the topic list command again:*
*we can see that the topics of ROS 1 are present here!* 🐻
```
ros2 topic list
```

![Screenshot_6](https://github.com/le9na/using-ros-bridge/assets/90223879/2e15c62f-7465-4e15-a177-b4c4dca7791e)

