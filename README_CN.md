# OpenFlex 驱动包

本目录存放 OpenFlex 安装脚本使用的、按平台划分的本地驱动包。

## 目录结构

```text
openflex_drivers/
├── 22.04-amd64-humble/       # Ubuntu 22.04 amd64 / ROS 2 Humble
├── 24.04-arm64-Jazzy-Jetson/ # Ubuntu 24.04 arm64 Jetson / ROS 2 Jazzy
├── LICENSE
├── README.md
├── README_CN.md
└── openflex_component.yaml
```

## 平台对应关系

| 主机平台 | ROS 2 发行版 | 驱动目录 | 脚本参数 |
| --- | --- | --- | --- |
| Ubuntu 22.04 amd64 | Humble | `22.04-amd64-humble/` | `--platform humble` |
| Ubuntu 24.04 arm64 Jetson | Jazzy | `24.04-arm64-Jazzy-Jetson/` | `--platform jazzy` |

只能安装与当前主机匹配的目录，不能混用两个目录中的驱动包。

## 完整包列表

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

## 使用脚本安装

执行与主机平台匹配的命令：

```bash
cd ~/openflex_all/openflex_ws/src/OpenFleX
chmod +x ./install_openflex_drivers_and_build.sh

# Ubuntu 22.04 amd64 / ROS 2 Humble
./install_openflex_drivers_and_build.sh --env --platform humble

# Ubuntu 24.04 arm64 Jetson / ROS 2 Jazzy
./install_openflex_drivers_and_build.sh --env --platform jazzy
```
