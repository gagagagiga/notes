# Ubuntu 筆記

## Stacer
https://github.com/oguzhaninan/Stacer

```bash
sudo add-apt-repository ppa:oguzhaninan/stacer -y
sudo apt-get update
sudo apt-get install stacer -y
```

## Faenza Icons
https://github.com/shlinux/faenza-icon-theme

### 安裝方法1
```bash
sudo add-apt-repository ppa:tiheum/equinox
sudo apt-get update && sudo apt-get install faenza-icon-theme
```

### 安裝方法2
```bash
git clone https://github.com/shlinux/faenza-icon-theme.git
cd faenza-icon-theme
sudo ./INSTALL
```

### 修改Grub開機預設項目

Ubuntu 23.10.1

參考自
https://blog.csdn.net/m0_59839672/article/details/119180437

```bash
sudo gnome-text-editor /etc/default/grub
```

GRUB_DEFAULT=0
GRUB_TIMEOUT_STYLE=hidden
GRUB_TIMEOUT=0

改成第五個項目windows開機

GRUB_DEFAULT=4
GRUB_TIMEOUT_STYLE=menu
GRUB_TIMEOUT=10


修改完grub後執行

```bash
sudo update-grub
```