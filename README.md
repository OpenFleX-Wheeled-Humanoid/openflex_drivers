# OpenFlex Drivers

This directory contains the platform-specific local driver packages used by the OpenFlex installer.

## Directory Structure

```text
openflex_drivers/
├── 22.04-amd64-humble/       # Ubuntu 22.04 amd64 / ROS 2 Humble
├── 24.04-arm64-Jazzy-Jetson/ # Ubuntu 24.04 arm64 Jetson / ROS 2 Jazzy
├── LICENSE
├── README.md
├── README_CN.md
└── openflex_component.yaml
```

## Platform Mapping

| Host platform | ROS 2 distribution | Driver directory | Installer option |
| --- | --- | --- | --- |
| Ubuntu 22.04 amd64 | Humble | `22.04-amd64-humble/` | `--platform humble` |
| Ubuntu 24.04 arm64 Jetson | Jazzy | `24.04-arm64-Jazzy-Jetson/` | `--platform jazzy` |

Only install the package set matching the host platform. Do not mix packages between the two directories.

## Package Lists

### Ubuntu 22.04 amd64 / ROS 2 Humble

```text
GTSAM-4.3.0-Linux.deb
livox-sdk2_2.0.0-1_amd64.deb
openflex-acados_0.1.0_amd64.deb
openflex-can-driver_1.0.0_amd64.deb
sophus_1.22.10-1_amd64.deb
openflex_driver-1.0.0-cp310-cp310-manylinux_2_17_x86_64.whl
```

### Ubuntu 24.04 arm64 Jetson / ROS 2 Jazzy

```text
libgtsam-dev_4.3.0-1_arm64.deb
livox-sdk2_arm64.deb
openflex-acados_0.1.0_arm64.deb
openflex-can-driver_1.0.0_arm64.deb
sophus_1.22.10-1_arm64.deb
openflex_driver-1.2.0-py3-none-any.whl
```

## Install with the Script

Run the command matching the host platform:

```bash
cd ~/openflex_all/openflex_ws/src/OpenFleX
chmod +x ./install_openflex_drivers_and_build.sh

# Ubuntu 22.04 amd64 / ROS 2 Humble
./install_openflex_drivers_and_build.sh --env --platform humble

# Ubuntu 24.04 arm64 Jetson / ROS 2 Jazzy
./install_openflex_drivers_and_build.sh --env --platform jazzy
```
