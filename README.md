# P5 LiveOps

本仓库用于公开分发 P5 公告和经过验收的客户端发布产物，不存放玩家数据、凭据或完整工程。

公告文件：`notice/p5-notice.json`，含同一份中英文测试公告。

客户端公告直链：

- GitHub: https://raw.githubusercontent.com/swordgrass/p5-liveops/main/notice/p5-notice.json
- Gitee: https://gitee.com/swordgrass/p5-liveops/raw/main/notice/p5-notice.json

## Windows 热更联调候选

文件位于 [`hotupdate/windows64-development/`](hotupdate/windows64-development/)，由实际构建产物生成，包含 `manifest.json`、`assemblies/`、`metadata/` 和 `bundles/`。

- 平台／通道：`Windows64`／`development`
- 补丁版本：`code-patch-r2`
- 匹配基包：`P5-base-20261107-player-r3`
- 106 个载荷文件，共 60,702,325 字节，已逐文件校验长度和 SHA-256。
- 这是联调候选；真实 Player 下载执行、镜像切换和失败回退尚未完成验收。
- GitHub 清单、DLL、元数据及最大资源包的匿名下载抽查通过。Gitee 仓库已同步，但约 14.7 MB 的资源包 Raw 下载返回 HTTP 403，要求登录；目前不能将它视为完整的免登录热更镜像。

更新清单直链：

- GitHub: https://raw.githubusercontent.com/swordgrass/p5-liveops/main/hotupdate/windows64-development/manifest.json
- Gitee: https://gitee.com/swordgrass/p5-liveops/raw/main/hotupdate/windows64-development/manifest.json
- Cloudflare: https://p5-telemetry.swordgrass-p5.workers.dev/hotupdate/windows64-development/manifest.json

客户端更新根地址是上述 `manifest.json` 的父目录。镜像必须逐文件保持相同字节，客户端按平台、通道、基包兼容身份及文件摘要检查。

公告内容变更时使用新 `version`；客户端拒绝以同一版本号替换不同文案。
