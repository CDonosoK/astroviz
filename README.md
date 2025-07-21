# AstroViz

<img src="https://github.com/CDonosoK/astroviz/blob/main/images/AstroViz.png" alt="AstroViz Image" width="800" height="400">

[![License](https://img.shields.io/badge/License-MIT--Clause-blue.svg)](https://opensource.org/licenses/MIT)
[![ROS2 Version](https://img.shields.io/badge/ROS-Humble-green)](https://docs.ros.org/en/humble/index.html)
[![GitHub Stars](https://img.shields.io/github/stars/CDonosoK/astroviz?style=social)](https://github.com/CDonosoK/astroviz/stargazers)


This is a ROS2 package designed for teleoperation, featuring a GPS map viewer and waypoint management. It allows users to visualize GPS data and manage waypoints for autonomous navigation. Aditionally, provides a camera viewer and a GUI to visualize the robot's state.

## Visual Overview
<table>
  <tr>
    <td colspan="2" align="center">
      <strong>DASHBOARD VIEWER</strong><br>
      <img src="https://github.com/CDonosoK/astroviz/blob/main/images/dashboard.gif" alt="Teleoperation Overview" width="800">
    </td>
  </tr>
</table>

For a detailed view of all implemented windows, see: [windows implemented](WINDOWS_IMPLEMENTED.md)

## Support 💖

If you find this project helpful and want to support its ongoing development, you can buy me a coffee! Every contribution helps me dedicate more time to improving and maintaining open-source software.

<a href="https://www.buymeacoffee.com/CDonosoK" target="https://buymeacoffee.com/cdonosok">
  <img src="https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white" alt="Buy Me a Coffee">
</a>


## Table of Contents
1. [Get Started](#get-started)
   - [Prerequisites](#prerequisites)
   - [Installation](#installation)
      - [Clone the Repository](#clone-the-repository)
      - [Build Using Docker](#build-using-docker)
      - [Run the Docker Container](#run-the-docker-container)
2. [Usage](#usage)
   - [Node Overview](#node-overview)
   - [Running Nodes](#running-nodes)
3. [Maintainer](#maintainer)
3. [License](#license)

---

## Get Started
### Prerequisites

To run this package, ensure the following dependencies are installed:
- **Git**: For version control and repository management.
- **Docker**: To streamline the environment setup and execution.
- **NVIDIA Container Toolkit** (if using an NVIDIA GPU): For hardware acceleration.


### Installation

#### Clone the Repository
Start by cloning the repository:
```bash
git clone git@github.com:CDonosoK/astroviz.git
```

#### Build Using Docker
This repository includes a pre-configured Docker setup for easy deployment. To build the Docker image:
1. Navigate to the `docker` directory:
   ```bash
   cd astroviz/docker
   ```
2. Run the build script:
   ```bash
   sh build.sh
   ```
   This will create a Docker image named `astroviz`.

#### Run the Docker Container
Once built, launch the container using:
```bash
sh run.sh
```
---

## Usage
### Node Overview

This package nodes that are designed to facilitate teleoperation and visualization of data. Each node serves a specific purpose in the teleoperation workflow:
- **gpsmap_viewer**: Visualizes GPS data on a map.
- **camera_viewer**: Displays camera feed from the robot.
- **imu_viewer**: Visualizes IMU data.
- **lidar_viewer**: Visualizes LiDAR data.
- **teleoperation_viewer**: Provides a GUI for teleoperation control.
- **dashboard_viewer**: A comprehensive dashboard that integrates various data streams and provides a unified interface for monitoring and control.
- **plot_viewer**: Displays real-time plots of various data streams.
- **grid_map_viewer**: Visualizes grid map data for navigation and planning.
- **robot_state_viewer**: Displays the current state of the robot related to the joint positions and transformations.
- **motor_state_viewer**: Monitors and visualizes the state of the robot's motors, including temperature and voltage readings.


### Running Nodes
To run the nodes, you can use the following command:
```bash
ros2 run astroviz <node_name>
```
Replace `<node_name>` with the name of the node you wish to run, such as `gps_map_viewer`, `camera_viewer`, etc.

Or if you prefer to run the dashboard viewer, which integrates all functionalities:
```bash
ros2 run astroviz dashboard_viewer
```

## Maintainer
This package is maintained by:

**Clemente Donoso**  
Email: [clemente.donosok@gmail.com](mailto:clemente.donosok@gmail.com)
GitHub: [CDonosoK](https://github.com/CDonosoK)  

---

## License
This project is licensed under the **MIT**. See the [LICENSE](LICENSE) file for details.

---
Contributions and feedback are welcome! If you encounter any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.