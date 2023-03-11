## 标准输出输出到剪贴板
[参考](https://blog.csdn.net/smalosnail/article/details/120589901)
```
pacman -S xsel
cat /path/to/file | xsel -b
xsel -b < /path/to/file
```
**注意事项：一定要选择正确的`Selection`，比如`clipboard`，不然无法生效！**
