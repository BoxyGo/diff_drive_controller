# diff_drive_controller – Middle Wheel Odometry

This repository provides a modified version of the `diff_drive_controller` for ROS 2, enabling odometry computation based solely on the **middle wheel** of each side instead of averaging all wheels.

## Features

- Uses **one wheel per side** (middle wheel) as the odometry source  
- Reduces odometry noise on multi-wheel skid-steer or 6-wheel platforms  
- Minimal changes, fully compatible with the original `diff_drive_controller` API  
- Enabled via a single configuration parameter

## Parameter

Enable middle-wheel odometry in your controller config:

```yaml
diff_drive_controller:
  ros__parameters:
    odom_middle_wheel_calc: true
    show_log: true
