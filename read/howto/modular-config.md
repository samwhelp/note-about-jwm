---
title: 模組化設定檔
nav_order: 7031
has_children: false
parent: 如何
---


# 模組化設定檔




## 主題

* [設定擋路徑](#設定擋路徑)
* [設定擋範例](#設定擋範例)
* [模組化說明](#模組化說明)




## 設定擋路徑

| 設定擋路徑 |
| --------- |
| [~/.jwmrc](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Main-Standalone/asset/overlay/etc/skel/.jwmrc) |




## 設定擋範例

| 設定擋範例 |
| --------- |
| [Main-Standalone](https://github.com/samwhelp/jwm-adjustment/tree/main/prototype/main/jwm-config/part/Main-Standalone) |
| [Main](https://github.com/samwhelp/jwm-adjustment/tree/main/prototype/main/jwm-config/part/Main) |
| [Modular-Basic](https://github.com/samwhelp/jwm-adjustment/tree/main/prototype/main/jwm-config/part/Modular-Basic) |
| [Modular-Port](https://github.com/samwhelp/jwm-adjustment/tree/main/prototype/main/jwm-config/part/Modular-Port) |
| [Modular-Profile](https://github.com/samwhelp/jwm-adjustment/tree/main/prototype/main/jwm-config/part/Modular-Profile) |




## 模組化說明

* [單一設定檔](#單一設定檔)
* [簡單拆分](#簡單拆分)
* [進階拆分](#進階拆分)




### 單一設定檔

關於「jwm」的設定檔，可以使用一個檔案搞定，路徑是「[~/.jwmrc](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Main-Standalone/asset/overlay/etc/skel/.jwmrc)」，格式是「`xml`」。

| 設定擋範例 |
| --------- |
| [Main-Standalone](https://github.com/samwhelp/jwm-adjustment/tree/main/prototype/main/jwm-config/part/Main-Standalone/asset/overlay/etc/skel) |




### 簡單拆分

我們可以將「jwm」的設定檔模組化，可以將設定拆分出去。

| 設定擋範例 |
| --------- |
| [Main](https://github.com/samwhelp/jwm-adjustment/tree/main/prototype/main/jwm-config/part/Main/asset/overlay/etc/skel) |

舉例：

* 我們可以將「Menu」的內容，拆分到「[$HOME/.config/jwm/menu](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Main/asset/overlay/etc/skel/.config/jwm/menu)」這個檔案，然後透過「`<Include>$HOME/.config/jwm/menu</Include>`」[這個指令加入](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Main/asset/overlay/etc/skel/.jwmrc#L19)

* 我們可以將「StartupCommand」裡面的[內容](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Main/asset/overlay/etc/skel/.jwmrc#L452-L456)，

``` sh
		nm-applet &

		variety &

		mate-volume-control-status-icon &
```

拆分到「[$HOME/.config/jwm/start](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Main/asset/overlay/etc/skel/.config/jwm/start)」這個檔案，然後透過「`<StartupCommand>~/.config/jwm/start</StartupCommand>`」[這個指令加入](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Main/asset/overlay/etc/skel/.jwmrc#L448)




### 進階拆分

我們也可以將「`xml`」的內容，拆分出去，請參考下面的範例。

| 設定擋範例 |
| --------- |
| [Modular-Basic](https://github.com/samwhelp/jwm-adjustment/tree/main/prototype/main/jwm-config/part/Modular-Basic/asset/overlay/etc/skel) |
| [Modular-Port](https://github.com/samwhelp/jwm-adjustment/tree/main/prototype/main/jwm-config/part/Modular-Port/asset/overlay/etc/skel) |
| [Modular-Profile](https://github.com/samwhelp/jwm-adjustment/tree/main/prototype/main/jwm-config/part/Modular-Profile/asset/overlay/etc/skel) |
