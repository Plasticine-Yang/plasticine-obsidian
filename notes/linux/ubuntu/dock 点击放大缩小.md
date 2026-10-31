# 问题

dock 栏的应用图标默认点击是打开，但再次点击不会缩小

# 解法

```shell
gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'
```

确认是否生效：

```shell
gsettings get org.gnome.shell.extensions.dash-to-dock click-action
# 应输出 'minimize'
```