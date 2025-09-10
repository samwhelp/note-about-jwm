---
title: 螢幕截圖
nav_order: 2051
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 螢幕截圖

* [透過「xfce4-screenshooter」](#xfce4-screenshooter)
* [透過「screengrab」](#screengrab)




## xfce4-screenshooter

| 按鍵組合       | 功能                 | 執行指令                                     |
| -------------- | -------------------- | -------------------------------------------- |
| `Print`        | 螢幕截圖             | `xfce4-screenshooter --fullscreen` |
| `Win + Print`  | 目前聚焦視窗截圖     | `xfce4-screenshooter --window`     |
| `Ctrl + Print` | 選取螢幕畫面區塊截圖 | `xfce4-screenshooter --region`               |
| `Alt + Print`  | 顯示截圖應用程式     | `xfce4-screenshooter`                        |


* [設定片段](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Modular-Basic/asset/overlay/etc/skel/.config/jwm/config/main/keybind/screenshot/via-xfce4-screenshooter.conf#L9-L12)

``` xml
	<Key key="Print">exec:xfce4-screenshooter --fullscreen</Key>
	<Key mask="4" key="Print">exec:xfce4-screenshooter --window</Key>
	<Key mask="C" key="Print">exec:xfce4-screenshooter --region</Key>
	<Key mask="A" key="Print">exec:xfce4-screenshooter</Key>
```

> 若是採用「`xfce4-screenshooter`」，在「Debian」，可以執行下面指令，安裝「[xfce4-screenshooter](https://packages.debian.org/stable/xfce4-screenshooter)」。

``` sh
sudo apt-get install xfce4-screenshooter
```




## screengrab

| 按鍵組合       | 功能                 | 執行指令                                     |
| -------------- | -------------------- | -------------------------------------------- |
| `Print`        | 螢幕截圖             | `screengrab --fullscreen` |
| `Win + Print`  | 目前聚焦視窗截圖     | `screengrab --active`     |
| `Ctrl + Print` | 選取螢幕畫面區塊截圖 | `screengrab --region`               |
| `Alt + Print`  | 顯示截圖應用程式     | `screengrab`                        |


* [設定片段](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Modular-Basic/asset/overlay/etc/skel/.config/jwm/config/main/keybind/screenshot/via-screengrab.conf#L9-L12)

``` xml
	<Key key="Print">exec:screengrab --fullscreen</Key>
	<Key mask="4" key="Print">exec:screengrab --active</Key>
	<Key mask="C" key="Print">exec:screengrab --region</Key>
	<Key mask="A" key="Print">exec:screengrab</Key>
```

> 若是採用「`screengrab`」，在「Debian」，可以執行下面指令，安裝「[screengrab](https://packages.debian.org/stable/screengrab)」。

``` sh
sudo apt-get install screengrab
```
