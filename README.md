# kebiao-releases

课表 / 电费客户端**发版产物仓库**（Public）。

## 这里放什么

- GitHub Release 附件：`kebiao-android-latest.apk`、`kebiao-windows-latest.exe`
- `dist/version.json` —— APP 用来检查最新版本的清单

## 这里不放什么

**不放任何源码、不放任何凭据、不放 keystore。**

源码在私有仓库 `kebiao-clients`。

## 为什么源码与产物要分开

GitHub 不支持「仓库私有但 Release 附件公开下载」——
私有仓库的 `releases/latest/download/...` 对未登录请求返回 **404**（已实测）。
所以发版产物必须放在公开仓库，APP 才能免登录自动更新。

## APP 读取地址

```
版本清单 : https://raw.githubusercontent.com/xiaozhuzi114514/kebiao-releases/main/dist/version.json
安装包   : https://github.com/xiaozhuzi114514/kebiao-releases/releases/latest/download/kebiao-android-latest.apk
```

## 发版

见 `deploy/gh_release.py`（后端团队提供的一键发版脚本）。
