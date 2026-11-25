# 篮球教练 PWA

手机上打开就是篮球训练工具，可加到主屏、离线可用。

**在线地址**：https://felicity-feng-dev.github.io/basketball/

## 仓库结构

| 路径 | 是什么 | 能不能手改 |
|---|---|---|
| index.html | 整个应用（界面 + 逻辑，单文件） | ❌ 别手改，会被下次发布覆盖 |
| sw.js | Service Worker：离线缓存，版本号 asketball-coach-vN 在这儿 | ❌ 同上 |
| manifest.webmanifest | 加到主屏用的名字 / 图标 / 主题色 | ❌ 同上 |
| .gitignore | 挡住运行日志、pid 这类临时产物 | ✅ |
| README.md | 本文件 | ✅ |
| docs/ | 开发说明（规则、发布流程） | ✅ |

> 这三个文件必须在仓库根目录：GitHub Pages 只从根发布，Service Worker 的作用域也只能覆盖它所在的目录。

## 怎么更新

改源码目录 ..\basketball-coach\ 下的同名文件 → 跑 发出去.ps1（或让 自动发布.ps1 常驻，改完静默 45 秒自动发）。

发布后等 30–60 秒生效；手机上可能要下拉刷新两次（Service Worker 换版本）。

## 本地预览

发布脚本会把最新三个文件同步到 工作区\_产出\，双击那里的 index.html 即可。
