ROS 2 (Robot Operating System)
=========

Ansible Role to install ROS2 Jazzy Jellyfish on Ubuntu Noble Numbat 24.04

Requirements
------------

Ubuntu 24.04


Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):


  ```yaml
  # Retrieved from ROS2 installation instructions
  ros_apt_source_api: https://api.github.com/repos/ros-infrastructure/ros-apt-source/releases/latest
  ros_apt_source_url: https://github.com/ros-infrastructure/ros-apt-source/releases/download

  # Options: jazzy (LTS); rolling
  ros2_distribution: jazzy

  # Options: desktop (recommended); ros-base (bare bones)
  ros2_configuration: desktop

  # Gazebo version to install
  GZ_VERSION: harmonic

  # Which RMW DDS implementation to use
  RMW_IMPLEMENTATION: rmw_cyclonedds_cpp


  # Default username and group for catkin_ws installation
  ros2_user:
      name: ubuntu
      group: ubuntu

  dev_ws: dev_ws

  ros2_domain_id: 0

  install_argcomplete: true

  # List of ROS packages to be installed without ros-<distro> prefix
  ros2_packages:
  ```


Dependencies
------------

None.

<!-- Example Playbook
----------------

Example to install ROS desktop-full configuration with turtlesim on the host system with a custom (existing) username:

```yaml
- hosts: localhost
  connection: local
  become: true
  vars:
    ros2_user:
        name: rarrais
        group: rarrais
    ros2_configuration: desktop
    ros2_packages:
      - turtlesim
  roles:
    - rarrais.ros2
``` -->

License
-------

MIT

Author Information
------------------

This role was created in 2025 by [zmdev2082](https://github.com/zmdev2082).
