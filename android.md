# Android 筆記


## 處理 小米 12T Pro 無限重啟的更新
新聞稿：https://m.eprice.com.tw/mobile/talk/4568/5807850/1/m/5807872

但是我的12T Pro 是HyperOS 在2024/4/5還是遇到無限重啟

根據 https://youtu.be/Dvg-Xqy9-I0?si=jndlNdQFCYzeNl4s 教學手動移除System UI Plugin

* 開啟cmd

* 至adb.exe 資料夾下
```
cd c:\Users\[User Folder]\AppData\Local\Android\Sdk\platform-tools
```

* 手機開啟 開發者模式、USB除錯

* 列舉裝置
```
adb devices
```

* 移除系統套件 System UI Plugin
```
adb shell pm uninstall -k --user 0 miui.systemui.plugin
```

* 移除完後，小米UI的功能，右上角下拉選單就失效了

參考網址：
* https://www.zhihu.com/question/512681245/answer/3068211492
* https://www.cnblogs.com/tangsong41/p/11069125.html
