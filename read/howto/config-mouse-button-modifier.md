---
title: 設定「Mouse Button Modifier」
nav_order: 7021
has_children: false
parent: 如何
---


# 設定「Mouse Button Modifier」




## 主題

* [相關文件](#相關文件)
* [說明](#說明)
* [相關議題](#相關議題)
* [相關應用](#相關應用)
* [相關連結](#相關連結)




## 相關文件

* Jwm / [Configuration](https://joewing.net/projects/jwm/config.html)




## 說明

原本的[設定](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Default-Debian/asset/overlay/etc/skel/.jwmrc#L182-L186)如下

``` xml
	<!-- The move mode (outline or opaque) -->
	<MoveMode>opaque</MoveMode>

	<!-- The resize mode (outline or opaque) -->
	<ResizeMode>opaque</ResizeMode>
```


等同於如下的設定，

也就是

| 按鍵組合 | 執行動作 |
| ------- | ------- |
| `Alt + [滑鼠左鍵拖曳]` | 視窗移動 |
| `Alt + [滑鼠右鍵拖曳]` | 視窗更改大小 |

> 關於「`mask="A"`」，指的是「`Alt鍵`」。

``` xml
	<MoveMode mask="A">opaque</MoveMode>

	<ResizeMode mask="A">opaque</ResizeMode>
```


而我慣用的「Mouse Button Modifier」是「`Win鍵`」，所以我會改成如下的[設定](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Main/asset/overlay/etc/skel/.jwmrc#L204-L213)

也就是

| 按鍵組合 | 執行動作 |
| ------- | ------- |
| `Win + [滑鼠左鍵拖曳]` | 視窗移動 |
| `Win + [滑鼠右鍵拖曳]` | 視窗更改大小 |

> 關於「`mask="4"`」，指的是「`Mod4鍵`」，也就是「`Win鍵`」或「`Super鍵`」。

``` xml
	<MoveMode mask="4">opaque</MoveMode>

	<ResizeMode mask="4">opaque</ResizeMode>
```


並且會加入「`coordinates="off"`」

``` xml
	<MoveMode mask="4" coordinates="off">opaque</MoveMode>

	<ResizeMode mask="4" coordinates="off">opaque</ResizeMode>
```


另外我還會補足一些[設定](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Main/asset/overlay/etc/skel/.jwmrc#L421-L426)如下，在「Window Title Bar」也能起作用。

``` xml
	<Mouse context="title" mask="4" button="1">move</Mouse>
	<Mouse context="title" mask="4" button="2">move</Mouse>
	<Mouse context="title" mask="4" button="3">resize</Mouse>
	<Mouse context="border" mask="4" button="1">move</Mouse>
	<Mouse context="border" mask="4" button="2">move</Mouse>
	<Mouse context="border" mask="4" button="3">resize</Mouse>
```




## 相關議題

| 相關議題 |
| ------- |
| [滑鼠按鍵綁定](https://samwhelp.github.io/note-about-jwm/read/config/mousebind.html#視窗內容區塊) |
| [設定按鍵綁定開啟「Main Menu」](https://samwhelp.github.io/note-about-jwm/read/howto/config-keybind-open-overlay.html) |




## 相關應用

* Menu Applet 開發筆記 / [demo-mouse-button-modifier](https://samwhelp.github.io/note-about-menu-applet/read/demo/demo-mouse-button-modifier.html#gnome-shell)




## 相關連結

* Jwm / [Configuration](https://joewing.net/projects/jwm/config.html)
