# WPI-Lidar-Visual-SLAM-Dataset

## Lidar Visual SLAM with Turtlebot 2

This Lidar Visual SLAM data was collected on the second floor of the Atwater Kent Lab, WPI, Worcester, MA, USA.

The collected dataset in Rosbag format. [[Download: 49.7 GB\]](https://computing.wpi.edu/WPI_VSLAM_dataset/2023-05-18-15-40-14_0.bag)

The sensor extrinsic calibration files (images and Lidar scan) between OS1-64 Lidar and Intel Realsense T265 camera. [[Download: 67.7 MB\]](https://computing.wpi.edu/WPI_VSLAM_dataset/calibrated_data_example.zip)

The camera intrinsic calibration files (images) for Intel Realsense T265 camera. [[Download: 26.5 MB\]](https://computing.wpi.edu/WPI_VSLAM_dataset/t265_stereo_calibration.zip)

The camera-imu calibration Rosbag with undistored images for Intel Realsense T265 camera. [[Download: 443MB]](https://computing.wpi.edu/WPI_VSLAM_dataset/camera_imu_calibration_data.bag)

The 3-hours static IMU Rosbag for Intel Realsense T265 camera. [[Download: 811MB]
](https://computing.wpi.edu/WPI_VSLAM_dataset/static_imu_data.bag)

### Example on Matlab:

Please also check the detail implementations with this dataset on Matlab examples:

* [Performant and Deployable Stereo Visual SLAM with Fisheye Images](https://www.mathworks.com/help/vision/ug/performant-and-deployable-stereo-visual-slam-with-fisheye-images.html)
* [Estimate Camera-to-IMU Transformation Using Extrinsic Calibration](https://www.mathworks.com/help/nav/ug/estimate-camera-to-imu-transformation-using-extrinsic-calibration.html)

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
