# 具身智能操作学习记录

更新：2026-09-23。方向：VLA、机器人操作、强化学习与 Isaac Lab。

当前主项目使用 SO101 leader/follower、双外部相机、LeRobot 与 SmolVLA，研究语言条件抓取、数据质量与真实执行之间的关系。已完成数据采集、微调、离线验证、云端推理和受限真机执行；最近两次完整同步尝试均未抓取成功。D1重新采集已准备，尚未完成。

## 阅读入口

- [项目一：实验结果与失败分析](PROJECT_01.md)
- [未来30天学习与项目计划](LEARNING_PLAN.md)
- [独立实现与面试验收](INTERVIEW_CHECKLIST.md)
- [Notion导入首页](NOTION_IMPORT.md)
- [同步状态与本地证据入口](SYNC_STATUS.md)

## 三个项目的定位

| 项目 | 要回答的问题 | 状态 |
|---|---|---|
| SO101语言条件操作与数据闭环 | 自采示范如何变成可靠的真实动作？ | 进行中；训练/执行链已通，抓取失败，准备D1 |
| Isaac Lab操作任务PPO与鲁棒性评估 | 奖励、观测、控制频率和随机化如何影响学习？ | 已有本地Reach/Lift工程，下一阶段核对与实验 |
| 示范辅助强化学习与数据效率 | 成功示范能否减少操作任务的在线交互量？ | 计划中；项目二稳定后启动 |

三个项目共用操作主题，但各自需要独立问题、对照和证据。第三项如果只完成学习练习，应如实作为扩展，不包装成完成的RL项目。

## 结果表述约定

“完成运行”不等于“成功抓取”；开发集loss不等于真机成功率；监督纠正数据微调不称为RL；在状态输入仿真里训练SAC不称为VLA后训练。本文档中的计划、用户报告、本地日志证据分别标明。

这份目录是项目文档归档，不是完整代码发行包。数据视频、权重及原始机器人配置保留在工作区；代码发布应保留第三方来源与许可证，并提供可配置的路径和硬件映射。

## 上游项目

- [LeRobot / SmolVLA](https://github.com/huggingface/lerobot)：主项目框架；当前本地安装显示0.4.5，复现仍需记录实际commit。
- [Isaac Lab v2.3.2](https://github.com/isaac-sim/IsaacLab/tree/v2.3.2)：沿用已有Isaac Sim 5.1环境，避免照抄新版本命令。
- [SO101 Isaac Lab工程](https://github.com/MuammerBay/isaac_so_arm101)：本地Reach/Lift工程的上游。
- [OpenPI](https://github.com/Physical-Intelligence/openpi)：用于π系列源码对比学习，本月不额外启动第二套大模型微调工程。
