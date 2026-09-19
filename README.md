# vcn-apk —— Venera 中文源版 发布仓库

这个仓库是给 **App 的「检查更新」功能**用的：App 会读取本仓库的 `pubspec.yaml` 比对版本号，
发现新版本就弹窗，点「更新」跳转到本仓库的 Releases 页下载新 APK。

- `pubspec.yaml` —— 版本号（App 读取这个文件判断是否有新版本）
- [Releases](../../releases) —— 各版本的 APK 安装包

## 版本号规则

`version: <语义化版本>+<构建号>`，例如 `1.6.3+1632`。
只有**大于**当前安装版本时，App 才会提示更新。

## 发布新版本

1. 改 `pubspec.yaml` 里的 `version`（如 `1.6.4+1640`）；
2. 在 Releases 里新建一个 tag（如 `v1.6.4`），把新 APK 作为附件上传；
3. App 端下次「检查更新」即可看到提示并下载。

## 说明

本仓库只放编译产物与版本号，不含漫画内容。漫画源规则在
[venera-cn-64bit](https://github.com/token1008/venera-cn-64bit)。
