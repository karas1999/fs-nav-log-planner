# Agent Instructions

本项目遵循共享 [Project Playbook](../project-playbook/PLAYBOOK.md)。非小型修改前阅读 Playbook、[PROJECT.md](PROJECT.md) 和 [README.md](README.md)，检查工作区后再读取实际可用的技能入口。

## 项目约束

- 当前存在 `skills/` 到 `.agents/skills/` 的未提交布局差异；不要擅自恢复删除文件、提交新版技能或决定迁移结果。
- 路书默认中文、用于模拟飞行；保留用户航线和速度约束，具体格式与默认值以实际使用的技能为准。
- 导航骨架优先于历史解说。核对逐段 ETE、连续引导线、大尺度终止特征和近似地标的辨识提示。
- 不编造精确地理或航空资料；无法核验时明确标记草稿或不确定项。除非用户要求，不获取实时天气。
- 新路书默认存入被忽略的 `navlogs/`，保留既有区域组织；不要把生成路书或本地资源批量纳入 Git。
