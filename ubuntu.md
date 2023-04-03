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


## Qt 開發環境

需要額外安裝的套件
```bash
sudo apt install build-essential
sudo apt install mesa-common-dev
```