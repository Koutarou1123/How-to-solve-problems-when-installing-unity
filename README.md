# How-to-solve-problems-when-installing-Unity

## 概要
このリポジトリは私がUnityインストール時に公式通りに行い詰まった箇所の解決方法を記す．
---

### 環境
- Linux
- Ubuntu20.04

 
1.手順 https://docs.unity3d.com/hub/manual/InstallHub.html#install-hub-linux

mistake command
```
sudo sh -c 'echo "deb [signedby=/usr/share/keyrings/Unity_Technologies_ApS.gpg] https://hub.unity3d.com/linux/repos/deb stable main" > /etc/apt/sources.list.d/unityhub.list'
```
上記のコマンドだと，NO_PUBKEYと言われてしまう．
<br>
<br>

correct command
```
sudo sh -c 'echo "deb [signed-by=/usr/share/keyrings/Unity_Technologies_ApS.gpg] https://hub.unity3d.com/linux/repos/deb stable main" > /etc/apt/sources.list.d/unityhub.list'
```


# REFERENCE
---
1. https://docs.unity3d.com/hub/manual/InstallHub.html#install-hub-linux
2. https://askubuntu.com/questions/1395684/unity3d-installation-issues-gpg-error-repository-not-signed?answertab=modifieddesc#tab-top
