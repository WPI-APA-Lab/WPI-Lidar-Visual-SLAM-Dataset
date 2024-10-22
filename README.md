# WPI-Lidar-Visual-SLAM-Dataset

## Lidar Visual SLAM with Turtlebot 2

This Lidar Visual SLAM data was collected on the second floor of the Atwater Kent Lab, WPI, Worcester, MA, USA.

The collected dataset in Rosbag format. [[Download: 49.7 GB\]](https://app.box.com/s/oc9tyo24ln700dbqcsm5956rvboqpi5j)

The sensor extrinsic calibration files (images and Lidar scan) between OS1-64 Lidar and Intel Realsense T265 camera. [[Download: 67.7 MB\]](https://app.box.com/s/glglhb99kz0bl65kolkik6f924iei6fe)

The camera intrinsic calibration files (images) for Intel Realsense T265 camera. [[Download: 26.5 MB\]](https://app.box.com/s/kuuuigsonbcmvf2e7fgfc9lh0viqrvkv)

The camera-imu calibration Rosbag with undistorted images for Intel Realsense T265 camera. [[Download: 443MB]](https://app.box.com/s/jetqena41v5et27vhcj1icz1b0al83gx)

The 3-hours static IMU Rosbag for Intel Realsense T265 camera. [[Download: 811MB]](https://app.box.com/s/duwgn8ub7xuptx5q5ectjj1xbcs7im5y)

### Example on Matlab:

Please also check the detail implementations with this dataset on Matlab examples:

* [Performant and Deployable Stereo Visual SLAM with Fisheye Images](https://www.mathworks.com/help/vision/ug/performant-and-deployable-stereo-visual-slam-with-fisheye-images.html)
* [Estimate Camera-to-IMU Transformation Using Extrinsic Calibration](https://www.mathworks.com/help/nav/ug/estimate-camera-to-imu-transformation-using-extrinsic-calibration.html)

We will apprecitate if you cite following paper while you are using our data in your academic research

```
Z. Huang, X. Zhang, A. Garcia and X. Huang, "A Novel, Efficient and Accurate Method for Lidar Camera Calibration," 2024 IEEE International Conference on Robotics and Automation (ICRA), Yokohama, Japan, 2024, pp. 14513-14519, doi: 10.1109/ICRA57147.2024.10611162. 


```


### Rostopic:

#### SLAM Rosbag:

    /camera/fisheye1/camera_info     15030 msgs    : sensor_msgs/CameraInfo

    /camera/fisheye1/image_raw       15029 msgs    : sensor_msgs/Image

    /camera/fisheye2/camera_info     15029 msgs    : sensor_msgs/CameraInfo

    /camera/fisheye2/image_raw       15029 msgs    : sensor_msgs/Image

    /camera/imu                     100202 msgs    : sensor_msgs/Imu

    /joint_states                    29998 msgs    : sensor_msgs/JointState     (2 connections)

    /mobile_base/sensors/imu_data    24988 msgs    : sensor_msgs/Imu

    /odom                            24987 msgs    : nav_msgs/Odometry

    /ouster/imu                      50093 msgs    : sensor_msgs/Imu

    /ouster/metadata                     1 msg     : std_msgs/String

    /ouster/points                   10019 msgs    : sensor_msgs/PointCloud2

    /ouster/range_image              10020 msgs    : sensor_msgs/Image

    /tf                             194952 msgs    : tf2_msgs/TFMessage         (4 connections)

    /tf_static                           1 msg     : tf2_msgs/TFMessage

#### Camera_imu_calibration_data Rosbag:

    /camera/camera_info       	1 msg     : sensor_msgs/CameraInfo

    /camera/image_raw       677 msgs    : sensor_msgs/Image(undistorted and resampled in 10Hz)

    /camera/imu           	13936 msgs    : sensor_msgs/Imu(200Hz)

#### Static-imu_data Rosbag (3hrs):

    /camera/imu   2160225 msgs    : sensor_msgs/Imu (200Hz)
