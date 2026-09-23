# 发布状态与证据索引

最新同步结果：用户重新连接GitHub后，写入已成功，README、项目报告、30天学习计划、面试清单及Notion导入文档均已上传并通过远端目录核对。Notion页面尚未创建。

整理日期：2026-09-23。

## 发布状态

- 本地文档已整理；GitHub主要文档已同步，本文件记录发布状态；Notion尚未同步。
- 用户已创建公开仓库[std-song/std-song-embodied-manipulation-lab](https://github.com/std-song/std-song-embodied-manipulation-lab)，开始上传前确认仓库为空，默认分支main。
- 插件查询确认Notion已安装且ENABLED，用户也确认MCP servers中存在Notion；当前会话仍未暴露Notion调用工具。这是会话工具可用性问题，不能断言用户没有安装。需要刷新连接/新会话暴露工具，并指定父页面后继续发布。
- 本次发布范围为本目录整理后的文档，不是完整代码发行包；原始数据视频、模型权重、服务器地址和硬件序列号未上传。

## 本地证据入口（相对于项目工作区根目录）

| 结论 | 证据位置 |
|---|---|
| 60条训练与12条dev | outputs/project_01_vla/datasets/d0_train_white_cup_red_cap_v1/meta/info.json；d0_dev_white_cup_red_cap_v1/meta/info.json |
| 5k训练与吞吐 | outputs/project_01_vla/results/cloud_baseline_d0_001/summary.json |
| 10k续训与9k best | outputs/project_01_vla/results/cloud_baseline_d0_extend_10k_001/summary.json |
| 真机003/004失败 | outputs/project_01_vla/results/sync_task_white_003/summary.json；sync_task_white_004/summary.json |
| 边界与标签分析 | outputs/project_01_vla/results/sync_task_white_004/analysis/boundary_audit.json |
| 三类动作偏差 | outputs/project_01_vla/results/sync_task_white_003/analysis/metrics.json |
| 当前采集命令 | plans/project_01_vla/D1_COLLECTION.md |
| 当前硬件数据协议 | plans/project_01_vla/D1_SETUP.json |
| 完整历史计划 | plans/project_01_vla/PLAN.md |

这些是本地审计索引，不承诺原始文件已公开。对外引用结果时附实验条件和限制；如发布精简证据，先移除主机路径与设备标识，并保留字段含义和原始来源。

## 恢复同步所需的最少操作

GitHub：写入权限已实际验证，无需再次修改授权。后续更新前读取远端当前版本，避免覆盖其他修改。

Notion：刷新已启用插件/MCP连接并开启能暴露Notion工具的新会话，提供父页面链接。以本目录README.md作为恢复入口，读取本文件确认哪些内容尚未同步。
