---
title: 設定按鍵綁定開啟「Main Menu」
nav_order: 7022
has_children: false
parent: 如何
---


# 設定按鍵綁定開啟「Main Menu」




## 相關文件

* Jwm / [Configuration](https://joewing.net/projects/jwm/config.html)




## 說明


### RootMenu

原本「RootMenu」的[設定](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Default-Debian/asset/overlay/etc/skel/.jwmrc#L5C2-L5C24)，是設定在「桌面」，「滑鼠左鍵單按」或「滑鼠中鍵單按」可以觸發開啟「Main Menu」。

``` xml
	<RootMenu onroot="12">
```

改成如下的[設定](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Main/asset/overlay/etc/skel/.jwmrc#L5)，改成在「桌面」，「滑鼠右鍵單按」可以觸發開啟「Main Menu」。

``` xml
	<RootMenu onroot="3">
```



## 額外的按鍵綁定

原本[設定](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Default-Debian/asset/overlay/etc/skel/.jwmrc#L203C2-L203C37)「`Alt + F1`」可以觸發開啟「Main Menu」。

``` xml
	<Key mask="A" key="F1">root:1</Key>
```

改成如下的[設定](https://github.com/samwhelp/jwm-adjustment/blob/main/prototype/main/jwm-config/part/Main/asset/overlay/etc/skel/.jwmrc#L238-L239)，設定成「`Alt + F1`」或「`Win + Space`」可以觸發開啟「Main Menu」

``` xml
	<Key mask="A" key="F1">root:3</Key>
	<Key mask="4" key="space">root:3</Key>
```




## 相關議題

| 相關議題 |
| ------- |
| [設定 Mouse Button Modifier](https://samwhelp.github.io/note-about-jwm/read/howto/config-mouse-button-modifier.html) |
