## linux 中文及emoji字体配置
需要安装这些包：
```sh
pacman -S noto-fonts-sc noto-fonts-emoji noto-fonts
```
然后刷新字体缓存：
```sh
fc-cache -vf
```
然后应该就可以了（？）部分字体可能没有立刻刷新，可能需要进行 `reboot` 大法

## linux 输入法配置
需要安装这些包：
```sh
pacman -S fcitx5 fcitx5-chinese-addons citx5-configtool fcitx5-gtk fcitx5-input-support fcitx5-qt 5.0.17-1
```
然后应该就可以了（？
