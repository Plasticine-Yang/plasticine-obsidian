
图形化方式 & 终端方式均可配置，无论哪种方式都需要配置完后 logout 再 login 才能生效

# 图形化方式

## 1. 安装 gnome-tweaks

```shell
sudo apt install gnome-tweaks
```

## 2. 交换按键

`Tweaks → 键盘 → 其他布局选项 → Ctrl 键位置`

选择交换 Caps 和 Ctrl 位置即可

# 终端方式

交换：

```shell
gsettings set org.gnome.desktop.input-sources xkb-options "['ctrl:swapcaps']"
```

恢复：

```shell
gsettings reset org.gnome.desktop.input-sources xkb-options
```

