# FS Nav Log Planner

面向飞行模拟器的 VFR 观光路书规划技能仓库。技能指导代理生成中文优先的 Markdown 路书：逐航段提供航向、距离与预计时间、连续视觉引导线、终止特征、驾驶舱辨识提示及简短历史解说。

## 使用

本项目是代理技能与文本资料，不是独立应用；没有安装依赖、启动服务或构建步骤。需要能加载 `SKILL.md` 的代理环境，以及用户提供的航线资料或可核验的地理资料。

技能入口为 [.agents/skills/vfr-routebook-planner/SKILL.md](.agents/skills/vfr-routebook-planner/SKILL.md)，界面配置位于其 `agents/openai.yaml`。将技能交给支持它的代理后，可请求：

```text
使用 vfr-routebook-planner，为指定出发机场到目的机场生成中文模拟飞行 VFR 观光路书。
```

技能默认使用 Draco X、120 kt 规划地速；用户明确要求慢速观光时可用 100 kt。默认输出保存在 `navlogs/`，该目录被 Git 忽略。实际航线、地形和距离应根据用户资料或来源核验；路书不替代真实飞行所需的正式资料和判断。

## 技能布局

技能统一位于 `.agents/skills/vfr-routebook-planner/`：`SKILL.md` 保留入口、默认值、工作流程和航段要求，`references/` 按需提供路书方法、资料核验边界和日本战国主题指导，`agents/openai.yaml` 定义界面名称与默认提示。旧的 `skills/vfr-routebook-planner/` 入口已移除。

## 验证

没有自动化测试或运行程序。修改技能后检查 `SKILL.md` 元数据、参考文件路径和界面配置；对示例路书核对每段航向、距离/ETE、引导线、终止特征、混淆排除和资料来源。使用 `ETE 分钟 = 航程 NM / 地速 kt × 60` 重新计算各段及合计。

## 项目文档

- [AGENTS.md](AGENTS.md)：工作入口与项目约束。
- [PROJECT.md](PROJECT.md)：当前状态、架构和交接事项。
- [CHANGELOG.md](CHANGELOG.md)：依据 Git 历史记录的里程碑。
