## KDE 下 vivaldi 等 chromium 内核浏览器暗黑模式问题

更新：在Chromium 114中修复了此问题，在更新到此版本以后可以不用此方法了。

---

KDE 下 vivaldi 等 chromium 内核浏览器暗黑模式有无法跟随系统主题的问题，这时需要一些其他办法来解决此问题。

1. 在启动参数中加入 `--force-dark-mode`
2. 在 [`chrome://flags`](chrome://flags) 中启用 `Auto Dark Mode for Web Contents` 实验性功能（实际体验并不是特别好，有一些内容被错误地变成了深色。）
