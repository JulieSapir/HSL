<p align="center">
<img src="./HSL.svg" alt="HSL logo" width=100/>
</p>

<h1 align="center">Hi Subsystem for Linux (HSL)</h1>

Hi Subsystem for Linux (HSL) 是一个用于在新操作系统上运行 Linux 应用程序的兼容层。通过模拟 Linux 系统环境而不是整个主机，HSL 能以极高的性能（99~99.8%）运行未修改的原生 Linux 应用程序。 和虚拟机不同， HSL 几乎没有额外开销且包含原生网络支持。

HSL 仅支持 ARM64 架构的 HarmonyOS/OpenHarmony 系统。

<p align="center">
<img src="./LAYER.svg" alt="LAYER" width=600/>
</p>

## 特性

- Ubuntu rootfs 支持
- sshd
- 完全的 root 权限
- Python3 兼容
- NodeJS 兼容
- GPU 加速支持
- IPv6 的原生网络套接字
- Windows ARM64 应用程序支持（通过wine）
- x11vnc
- JIT-less模式 基于[QEMU](https://github.com/harmoninux/qemu)

## TODO

- 修复坏掉的pty
- 添加等宽字体[JetBrains Maple Mono](https://github.com/SpaceTimee/Fusion-JetBrainsMapleMono)
- 重构C++测试集
- 可更换自定义镜像
- 挂载或从外部访问EXT4文件系统
    - 可修改大小的稀疏镜像
    - 碎片整理功能
- (仅PC端)使用[yserver](https://github.com/joske/yserver)作为x11后端
    - 启动菜单及系统托盘
    - x11原生窗口渲染（undercover风格）
    - 仿explorer的文件管理器UI
    - Proton直通OHNativeWindow
- OpenJDK 兼容性
- Windows x86\_64 应用程序
- Linux x86\_64 应用程序 (目前通过 box64 以支持命令行程序, 正在向 FEX 迁移以获得更高性能)

## 可能支持

- Docker (也许需要重度修改才能运行)

## 顺便一提

1. 早期 HSL 使用 WebAssembly 提供真正的 Linux 内核，但后来被证明并不需要塞一个内核进去也能用。
2. V社两周前发布了他们第一款ARM64设备，意味着Proton后续会加强ARM64的支持，这对HSL来说是好事，特别是对Windows游戏的兼容性。你真的可以期待以后在鸿蒙PC上玩大型3A。
3. 在找完整的 Linux ？看看[HiSH](https://github.com/harmoninux/hiSH)吧

## Credits

Original Tux image by Larry Ewing <lewing@isc.tamu.edu>, created with The GIMP. Modified by JulieSapir.
