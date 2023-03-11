## 通过调整cpu频率来提高续航
[参考](https://wiki.archlinuxcn.org/wiki/CPU_%E8%B0%83%E9%A2%91#cpupower)
1. 安装 `cpupower`：
```sh
pacman -S cpupower
# 也可以安装GUI
yay -S cpupower-gui
```
2. 启动  `cpupower`
```sh
systemctl enable cpupower --now
```

3. 设置 cpu 调速器
```sh
cpupower frequency-set -g ${governor}
```
下面是 cpu 调速器的列表：
调速器 | 描述
-|-
performance | 运行于最大频率，数值一般为CPU最大频率。
powersave | 运行于最小频率，数值一般为CPU最小频率。
userspace | 运行于用户指定的频率，通过 `/sys/devices/system/cpu/cpu*/cpufreq/scaling_setspeed` 配置。
ondemand | 按需快速动态调整CPU频率， 一有cpu计算量的任务，就会立即达到最大频率运行，空闲时间增加就降低频率。此调速器的调速策略较为激进。
conservative | 按需快速动态调整CPU频率， 比 ondemand 的调整更保守。
schedutil | 基于[调度程序](https://lwn.net/Articles/682391/)调整 CPU 频率。
