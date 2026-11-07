# P5 LiveOps

本仓库用于公开分发 P5 公告和经过验收的客户端发布产物，不存放玩家数据、凭据或完整工程。

当前准备内容：`notice/p5-notice.json`，含同一份中英文测试公告。测试公告仅用于验证公告下载和显示，不代表游戏版本更新。

客户端公告直链（发布到 `main` 后由集成人验证）：

- GitHub: https://raw.githubusercontent.com/swordgrass/p5-liveops/main/notice/p5-notice.json
- Gitee: https://gitee.com/swordgrass/p5-liveops/raw/main/notice/p5-notice.json

热更发布目录需由真实构建产物生成，其中包含 `manifest.json`、`assemblies/`、`metadata/` 和 `bundles/`。未取得对应基包及验收发布物前不生成占位清单。镜像必须逐文件保持相同字节。

公告内容变更时使用新 `version`；客户端拒绝以同一版本号替换不同文案。
