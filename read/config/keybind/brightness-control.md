---
title: 螢幕亮度控制
nav_order: 5053
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 螢幕亮度控制




## 按鍵組合一

| 按鍵組合          | 功能             | 執行指令                                    |
| ----------------- | ---------------- | ------------------------------------------- |
| `Alt + Shift + [` | 減少螢幕亮度         | `brightnessctl set 5%-` |
| `Alt + Shift + ]` | 增加螢幕亮度         | `brightnessctl set +5%` |

* [設定片段](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Modular-Basic/asset/overlay/etc/skel/.config/jwm/config/main/keybind/brightness/via-brightnessctl.conf#L11-L12)

``` xml
	<Key mask="AS" key="bracketleft">exec:brightnessctl set 5%-</Key>
	<Key mask="AS" key="bracketright">exec:brightnessctl set +5%</Key>
```




## 按鍵組合二

| 按鍵組合               | 功能           | 執行指令                                    |
| ---------------------- | -------------- | ------------------------------------------- |
| `Monitor Brightness Up` | 減少螢幕亮度       | `brightnessctl set 5%-` |
| `Monitor Brightness Down` | 增加螢幕亮度       | `brightnessctl set +5%` |

* [設定片段](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Modular-Basic/asset/overlay/etc/skel/.config/jwm/config/main/keybind/brightness/via-brightnessctl.conf#L9-L10)

``` xml
	<Key key="XF86_MonBrightnessUp">exec:brightnessctl set 5%-</Key>
	<Key key="XF86_MonBrightnessDown">exec:brightnessctl set +5%</Key>
```




> 我的筆電按鍵

| 按鍵組合               | 功能           | 執行指令                                    |
| ---------------------- | -------------- | ------------------------------------------- |
| `Fn + F5` | 減少螢幕亮度       |  |
| `Fn + F6` | 增加螢幕亮度       |  |
| `Fn + F7` | 開啟或關閉螢幕       |  |




## 用法對照

* [音量控制](https://samwhelp.github.io/note-about-jwm/read/config/keybind/volume-control.html)
