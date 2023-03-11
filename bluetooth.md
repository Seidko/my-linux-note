## 音频蓝牙设备无法连接
需要安装这些包：
```
pacman -S bluez bluez-libs bluez-utils pulseaudio-bluetooth
```
这样音频设备就能被识别到了！
根据后续分析，`pulseaudio-bluetooth`包起到了最核心的作用，我猜测视频蓝牙设备或者其他蓝牙设备需要装对应的驱动。
