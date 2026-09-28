# OpenFlex Drivers

This directory stores the local dependency and driver packages required by OpenFlex during installation.

The recommended method is to install everything through the installer script:

```bash
cd ~/openflex_all/openflex_ws/src/OpenFlex
chmod +x ./install_openflex_drivers_and_build.sh
./install_openflex_drivers_and_build.sh
```

The script automatically scans and installs:

- `*.deb`
- `*.whl`

## Package List

### 1. `livox-sdk2_2.0.0-1_amd64.deb`

What it is:
- Livox SDK2 package

What it is used for:
- provides the low-level SDK required by the chassis lidar stack
- used by functions such as `livox_ros_driver2`

How to install:
- recommended: use the installer script
- manual install:

```bash
sudo apt install ./livox-sdk2_2.0.0-1_amd64.deb
```

### 2. `openflex-acados_0.1.0_amd64.deb`

What it is:
- acados package used by OpenFlex

What it is used for:
- provides the acados runtime libraries and headers used by the project
- required by control-related modules that depend on acados

How to install:
- recommended: use the installer script
- manual install:

```bash
sudo apt install ./openflex-acados_0.1.0_amd64.deb
```

### 3. `openflex-can-driver_1.0.0_amd64.deb`

What it is:
- low-level OpenFlex CAN communication driver package

What it is used for:
- provides the communication libraries for the chassis and lift-slide
- provides the `openflex_can` system library and CMake config used during workspace builds

How to install:
- recommended: use the installer script
- manual install:

```bash
sudo apt install ./openflex-can-driver_1.0.0_amd64.deb
```

### 4. `openflex_driver-1.0.0-cp310-cp310-manylinux_2_17_x86_64.whl`

What it is:
- Python driver package for OpenFlex

What it is used for:
- provides Python-side driver access and interfaces
- used by features that depend on the Python driver layer

How to install:
- recommended: use the installer script
- manual install:

```bash
pip3 install --user ./openflex_driver-1.0.0-cp310-cp310-manylinux_2_17_x86_64.whl
```

## Recommendation

For normal use, run the installer script directly instead of installing each package one by one.

## License

This package is licensed under Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0).

Copyright (c) 2026 Chengdu Changshu Robot Co., Ltd.

For details, please refer to the [LICENSE](LICENSE) file or visit: http://creativecommons.org/licenses/by-nc-sa/4.0/

## Acknowledgments

This package is part of the OpenFlex full-body humanoid robot platform ecosystem, developed specifically for research and industrial applications in the humanoid robotics field.

---

## 📞 Contact Us

### Chengdu Changshu Robot Co., Ltd.
**Chengdu Changshu Robotics Co., Ltd.**

| Contact | Information |
|---------|-------------|
| 📧 Email | openarmrobot@gmail.com |
| 📱 Phone/WeChat | +86-17746530375 |
| 🌐 Website | https://openarmx.com/ |
| 🌐 Docs | http://docs.openarmx.com/ |
| 📍 Address | Tianjin Xiqing District · Daochao Robot Experience Base (City of Tomorrow) · Tianjin Humanoid Robot Center |
| 👤 Contact Person | Mr. Wang |
