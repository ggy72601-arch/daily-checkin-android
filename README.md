# 日常打卡助手 Android 项目

这是一个将现有网页界面封装进 Android WebView 的项目。项目包含 GitHub Actions 工作流，可在云端构建调试 APK。

## 用手机获取 APK（不需要电脑）

1. 下载项目 ZIP 并解压。
2. 在 GitHub 网站创建一个新的 **Public** 仓库（公开仓库可用免费 Actions），名称例如 `daily-checkin-android`。
3. 在仓库页面选择 **Add file → Upload files**，把解压后的项目文件和隐藏的 `.github/workflows/build-apk.yml` 一并上传。手机网页可能隐藏以点开头的文件夹；若看不到 `.github`，请先启用文件管理器“显示隐藏文件”，或者在 GitHub 网页端创建该工作流文件。
4. 提交到 `main` 分支后，打开仓库的 **Actions** 标签页，选择 **Build Android APK** 工作流，等待完成。
5. 打开成功的运行记录，在 **Artifacts** 区域下载 `daily-checkin-debug-apk`，解压后得到 `app-debug.apk`。
6. 在手机上点击 APK 安装。若 Android 提示权限，只对你信任的来源允许“安装未知应用”。

## 重要说明

- 这是 debug APK，适合个人测试，不是发布到应用商店的正式签名版本。
- GitHub Actions 的界面可能随设备和语言略有不同。
- APK 的构建依赖在线服务；仓库里不要上传任何密码、密钥或个人敏感资料。
