# 安心清理 · 官方下载

本仓库提供安装包、版本说明和 SHA256 校验和。应用源码保存在独立的私有仓库，本仓库不包含源码。

**[进入最新版下载页面](https://github.com/BiQing-hc/anxin-disk-care-downloads/releases/latest)**

| 电脑 | 下载文件 | 安装位置 |
| --- | --- | --- |
| Windows 10 / 11，64 位 Intel / AMD | `AnxinDiskCare-…-Windows-x64-Setup.exe` | 当前用户的 `%LOCALAPPDATA%\Programs\AnxinDiskCare`，开始菜单可打开 |
| Windows 便携版 | `AnxinDiskCare-…-Windows-x64.zip` | 完整解压后运行 `AnxinDiskCare.exe`；保留 `_internal` |
| macOS 14 或以上，Apple Silicon / Intel | `AnxinDiskCare-…-macOS-universal.pkg` | `/Applications/安心清理.app` |

不创建桌面快捷方式。更新前退出旧版，个人偏好与清理记录保留。Windows ARM 与 32 位系统未单独验证。

## 怎么使用

1. 选择源码项目目录，再点击扫描。没有 API Key 也能查看结果、手动选择与确认。
2. 可选：在 **API 设置** 中保存自己的 DeepSeek Key。macOS 使用系统钥匙串，Windows 使用系统凭据管理器。不要在聊天或指令里粘贴 Key。
3. 输入整理目标。只有本次明确许可并点击分析时，才向配置的服务发送指令和脱敏摘要；不发送文件正文。请勿在指令中填写敏感信息。
4. AI 只解释并标记建议，由你勾选并最终确认。项目依赖清理还须确认重新安装或构建的影响。

照片、视频、图库、剪映素材与草稿、微信和 QQ 数据、离线歌曲始终保护。未知数据保持只读，不能关闭保护。仅清理逐文件核验通过的代码，**不承诺移除整个 node_modules / .next**；保留的媒体与本地修改需在后续干净重装前另行备份。

## 两个平台的范围

| 功能 | macOS 原生版 | Windows 首版 |
| --- | --- | --- |
| 本机目录/项目占用查看 | 支持 | 支持 |
| 已核验 node_modules / .next 代码的手动清理 | 支持 | 支持，条件不足时只读 |
| DeepSeek / 自定义兼容接口、指令框与人工确认 | 支持 | 支持 |
| 针对 macOS 应用的精确缓存规则 | 支持 | 不适用，不扫描对应规则 |
| 只读 JSON CLI | 支持 | 支持 |

修改时间不代表最后使用时间，目录大小也不等于可释放空间。Windows 为保证安全，检测到开发进程或无法核对使用状态时可能保留整个候选项；请看界面具体原因。

## 下载核验

每个 Release 提供 `SHA256SUMS.txt`，与安装包一起下载。macOS 可运行 `shasum -a 256 安装包.pkg`；Windows PowerShell 可运行 `Get-FileHash 安装包.exe -Algorithm SHA256`，与清单逐字比较。

当前版本未包含商业代码签名证书或 Apple 公证，系统可能提示未知发布者。请确认下载来源并核对校验和，按系统提供的单个应用确认方式处理；无需关闭系统保护。

使用许可见 [LICENSE.txt](LICENSE.txt)。问题可在本仓库提交 Issue；请勿上传 API Key、聊天记录、私人扫描报告或含个人路径的截图。
