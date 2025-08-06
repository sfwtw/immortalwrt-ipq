# ImmortalWrt IPQ - 自建 Fork 仓库

这是一个基于 OpenWrt 的自定义固件项目，专门针对 IPQ 系列芯片优化。本仓库合并了多个上游项目的优秀特性，并加入了自定义的功能增强。

## 项目简介

本项目是基于以下上游仓库的自建 fork：

- [qosmio/openwrt-ipq](https://github.com/qosmio/openwrt-ipq) - IPQ 芯片优化版本
- [immortalwrt/immortalwrt](https://github.com/immortalwrt/immortalwrt) - ImmortalWrt 主线版本

### 主要特性

- 🚀 针对 IPQ 系列芯片深度优化
- 🔧 集成 ImmortalWrt 的增强功能
- 📦 添加个性化设置
- 🌐 添加Qmodem等插件支持
- 🔄 定期同步上游更新

## 支持的设备

- IPQ807x Night-CPE
- 其他设备不一定好用 争对我自己的设备做的优化

## 快速开始

### 系统要求

- Ubuntu 18.04/20.04/22.04 或其他 Linux 发行版
- 至少 4GB RAM
- 至少 25GB 可用磁盘空间

### 编译环境准备

```bash
# 安装依赖包
sudo apt update
sudo apt install build-essential clang flex bison g++ gawk \
gcc-multilib g++-multilib gettext git libncurses5-dev libssl-dev \
python3-distutils rsync unzip zlib1g-dev file wget

# 克隆仓库
git clone https://github.com/sfwtw/immortalwrt-ipq.git
cd immortalwrt-ipq

# 更新 feeds
./scripts/feeds update -a
./scripts/feeds install -a
```

### 编译固件

```bash
# Night-CPE 配置编译选项
make menuconfig

# 开始编译
make -j$(nproc) download
make -j$(nproc) V=s
```

## 自定义功能

本仓库在上游基础上添加了以下自定义功能：

- 🔐 增强的防火墙规则
- 📊 系统监控面板
- 🔧 一键优化脚本
- 📱 移动端管理界面优化
- 🌍 多语言支持增强

## 许可证

本项目基于 GPL-2.0 许可证开源，详见 [LICENSE](LICENSE) 文件。

## 致谢

感谢以下项目的贡献：

- [OpenWrt Project](https://openwrt.org/)
- [ImmortalWrt Team](https://github.com/immortalwrt/immortalwrt)
- [qosmio](https://github.com/qosmio/openwrt-ipq)
- 所有为开源路由器固件做出贡献的开发者们

## 免责声明

本固件仅供学习和研究使用，使用者需自行承担相关风险。请在使用前仔细阅读相关文档，确保了解刷机风险。

---

⭐ 如果这个项目对你有帮助，请给个 Star 支持一下！
