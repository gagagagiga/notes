# Windows 筆記

## 控制台、設定 捷徑
新增捷徑，右鍵內容，捷徑頁籤修改成以下設定
1. 快捷命令參考 [Ms-Settings URI Commands](https://woshub.com/ms-settings-uri-commands-windows-11/)
2. 圖示操考 [Windows icons locations](https://www.digitalcitizen.life/where-find-most-windows-10s-native-icons/)

* 音量混音程式
    * 目標: C:\Windows\explorer.exe ms-settings:apps-volume
    * 變更圖示: %systemroot%\system32\mmres.dll

* 電源選項
    * 目標: C:\Windows\explorer.exe C:\Windows\System32\powercfg.cpl
    * 變更圖示: %systemroot%\system32\ddores.dll

* 藍芽與裝置
    * 目標: C:\Windows\explorer.exe ms-settings:connecteddevices
    * 變更圖示: %systemroot%\system32\setupapi.dll

## Edge InPrivate視窗捷徑
[How to Create InPrivate Browsing Shortcut for Microsoft Edge Chromium](https://www.tenforums.com/tutorials/153406-how-create-inprivate-browsing-shortcut-microsoft-edge-chromium.html)

* 目標: "C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe" -inprivate -new-window http://whosnumber.com/tw/


## 管理 Windows Defender Credential Guard

https://learn.microsoft.com/zh-tw/windows/security/identity-protection/credential-guard/credential-guard-manage

## Total Commander

### 工具列設定：

* CodeCompare 目錄比較
    * Command: "C:\Program Files\Devart\Code Compare\CodeCompare.exe"
    * Parameters: "%X%P" "%X%T"

* CodeCompare 選取檔案比較
    * Command: "C:\Program Files\Devart\Code Compare\CodeCompare.exe"
    * Parameters: "%X%P%S" "%X%T%R"

* 選擇相同檔名
    * Command: cm_FocusSrc,cm_CopyNamesToClip,cm_FocusTrg,cm_LoadSelectionFromClip

* XnViewMP
    * Command: "C:\Program Files\XnViewMP\xnviewmp.exe"
    * Parameters: "%P%S"

* Git
    * Command: "C:\Program Files\Git\git-cmd.exe"
    * Parameters: /K "cd /d %T"

Icon file:
C:\totalcmd\WCMICONS.DLL

### 檔案列表自訂欄位
cm_SrcCustomView1
自訂欄位顯示，包含註解


## XnViewMP
設定 > 檢視 > 資訊
{Filename With Ext} - {Size KB} KB
{Width}x{Height} {Zoom}%
{EXIF:Date Taken}
{EXIF:Model}
{META:LensID}
{EXIF:Focal Length 35mm}mm - f{EXIF:F-Number} -  {EXIF:Exposure Time} - ISO{EXIF:ISO Value}

## 停止更新 Windows 10/11 選用更新項目

[下載](wushowhide.diagcab)


## 如何修復 Windows 10 中的 MBR？

進入“進階選項”螢幕後，點擊“命令提示字元”以啟動它。然後鍵入命令 bootrec.exe並按回車鍵，查看可用於此工具的選項。（有四個參數可用：/FixMbr、/FixBoot、/ScanOs 和 /RebuildBcd。每個參數都可以幫助您解決不同的啟動問題。

https://www.diskpart.com/tw/windows-10/fix-mbr-windows-10.html


## Mount or Unmount VHD or VHDX File

### 掛載：
```
Mount-VHD -Path "Full\path\to\vhd\file"
```

### 卸載：
```
Get-VHD -Path "Full\path\to\vhd\file"
Dismount-VHD -DiskNumber <number>
```

https://winaero.com/mount-or-unmount-vhd-or-vhdx-file-in-windows-10/

## How to add or remove a Open in Windows Terminal as administrator context menu for all users in Windows 11

### Add Expandable Right Click "Open in Windows Terminal as administrator" Context Menu
[下載](powershell/Add_expandable_Open_in_Windows_Terminal_as_administrator.reg)

### Add "Open in Windows Terminal as administrator" Context Menu
[下載](powershell/Add_Open_in_Windows_Terminal_as_administrator.reg)

### Remove "Open in Windows Terminal as administrator" Context Menu
[下載](powershell/Remove_Open_in_Windows_Terminal_as_administrator.reg)


https://www.elevenforum.com/t/add-open-in-windows-terminal-admin-context-menu-in-windows-11.581/