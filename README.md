# ROS2_object_detection_using_PCL

### Design and algorithm

1. Detect from clustering
    Unsupervised euclidean cluster extraction
2. Track
    tracking (object ID & data association) with an ensemble of Kalman Filters
3. Classify static and dynamic object


### Installation
`colcon build`

### Usage

`ros2 run pcl_object_detection pcl_object_detection --ros-args --param-file config/config.yaml`

### Topics

Subscriptions:
- Name: `/filtered_clouds`
Type: `sensor_msgs::msg::PointCloud2`

Publishers:

- Name: `viz`     Type:`visualization_msgs::msg::MarkerArray`

- Name: `cluster`
Type: `sensor_msgs::msg::PointCloud2`

- Name: `obj_id`
Type: `std_msgs::msg::Int32MultiArray`
