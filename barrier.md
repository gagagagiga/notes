# Barrier 2.4 設定
參考網址
* https://blog.csdn.net/fgh544568/article/details/124854936
* https://github.com/debauchee/barrier/issues/1377

## Windows 11

* Barrier 
    - https://sourceforge.net/projects/barrier.mirror/files/
    - https://github.com/debauchee/barrier

* Bonjour SDK for Windows
    - https://developer.apple.com/bonjour/

* OpenSSL
    - https://slproweb.com/products/Win32OpenSSL.html

* 安裝路徑，增加到環境變數Path中
c:\Program Files\OpenSSL-Win64\bin

* 如果Barrier顯示 SSL Fingerprint: Disabled
開啟PowerShell，在C:\Users\ [ username ]\AppData\Local\Barrier\SSL 執行以下命令重新產生

```
openssl req -x509 -nodes -days 365 -subj /CN=Barrier -newkey rsa:4096 -keyout Barrier.pem -out Barrier.pem
```
* 防火牆
Windows Defender防火牆 > 進階設定 > 輸入規則 >新增規則...
    * 程式集：%ProgramFiles%\Barrier\barriers.exe
    * 通信協定類型：TCP
    * 本機連接port：24800
    * 設定檔：網域、私人、公用



## Ubuntu 22.04

```
sudo apt install barrier -y
```

在wayland 模式下滑鼠會無法顯示，登入時要切換成 Xorg模式