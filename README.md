# frida-ssl-pinning
本项目为frida js 项目。主要为解决抓包过程中的SSL-PINNING 问题。  
ssl-pinning有单向验证及双向验证  
单向验证可通过 xposed 模块解决。也可使用frida hook解决。
双向验证必须要获取ssl证书，将证书安装到抓包工具中。
### 单向验证脚本  
frida-android-repinning.js 使用证书替换的方式劫持ssl-pinning。
### 双向验证脚本
frida-extract-keystore.py 嗅探证书并导出。原文见 http://ceres-c.it/frida-android-keystore/
