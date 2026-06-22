# OpenFlex Drivers 说明

本目录存放 OpenFlex 安装时需要用到的本地依赖包和驱动包。

推荐直接使用安装脚本统一安装：

```bash
cd ~/openflex_all/openflex_ws/src/OpenFlex
chmod +x ./install_openflex_drivers_and_build.sh
./install_openflex_drivers_and_build.sh
```

安装脚本会自动扫描并安装本目录下的：

- `*.deb`
- `*.whl`

## 包说明

### 1. `livox-sdk2_2.0.0-1_amd64.deb`

作用：
- Livox 雷达 SDK2 安装包

用途：
- 给底盘雷达相关功能提供底层 SDK
- 供 `livox_ros_driver2` 等相关功能使用

安装方式：
- 推荐通过安装脚本自动安装
- 也可以手动安装：

```bash
sudo apt install ./livox-sdk2_2.0.0-1_amd64.deb
```

### 2. `openflex-acados_0.1.0_amd64.deb`

作用：
- OpenFlex 使用的 acados 安装包

用途：
- 提供工程中用到的 acados 运行库和头文件
- 供依赖 acados 的控制相关模块使用

安装方式：
- 推荐通过安装脚本自动安装
- 也可以手动安装：

```bash
sudo apt install ./openflex-acados_0.1.0_amd64.deb
```

### 3. `openflex-can-driver_1.0.0_amd64.deb`

作用：
- OpenFlex 底层 CAN 通信驱动库安装包

用途：
- 提供底盘与升降台相关的底层通信库
- 提供工作空间编译时要用到的 `openflex_can` 系统库与 CMake 配置

安装方式：
- 推荐通过安装脚本自动安装
- 也可以手动安装：

```bash
sudo apt install ./openflex-can-driver_1.0.0_amd64.deb
```

### 4. `openflex_driver-1.0.0-cp310-cp310-manylinux_2_17_x86_64.whl`

作用：
- OpenFlex 的 Python 驱动包

用途：
- 提供 Python 侧的驱动与调用能力
- 供整机中依赖 Python 驱动的功能使用

安装方式：
- 推荐通过安装脚本自动安装
- 也可以手动安装：

```bash
pip3 install --user ./openflex_driver-1.0.0-cp310-cp310-manylinux_2_17_x86_64.whl
```

## 建议

正常使用时，直接运行安装脚本即可，不建议手动逐个安装。

## 许可证

本包通过 知识共享 署名-非商业性使用-相同方式共享 4.0 国际许可协议 (CC BY-NC-SA 4.0) 进行许可。

版权所有 (c) 2026 成都长数机器人有限公司 (Chengdu Changshu Robot Co., Ltd.)

详情请参阅 [LICENSE](LICENSE) 文件或访问：http://creativecommons.org/licenses/by-nc-sa/4.0/

## 致谢

本包是 OpenFlex 全身人形机器人平台生态系统的一部分，专为人形机器人领域的研究和工业应用而开发。

---

## 📞 联系我们

### 成都长数机器人有限公司
**Chengdu Changshu Robotics Co., Ltd.**

| 联系方式 | 信息 |
|---------|------|
| 📧 邮箱 | openarmrobot@gmail.com |
| 📱 电话/微信 | +86-17746530375 |
| 🌐 官网 | https://openarmx.com/ |
| 🌐 文档 | http://docs.openarmx.com/ |
| 📍 地址 | 天津市西青区・稻潮机器人体验基地（明日之城）・天津市人形机器人中心 |
| 👤 联系人 | 王先生 |
