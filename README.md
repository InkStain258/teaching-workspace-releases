# 教学工作空间 · 发布仓库

这里只放**安装程序与版本清单**，源码在私有仓库。

| 分支 | 产品 | 清单 |
|---|---|---|
| `yuwen` | 高中语文工作空间 | [`latest.json`](../../raw/yuwen/latest.json) |
| `general` | 教师工作空间 | [`latest.json`](../../raw/general/latest.json) |

程序的「设置 → 更新」会读对应分支的 `latest.json`，比对版本后下载同分支的安装包，
`certutil` 校验 SHA256 通过才静默安装，装完自动重新打开，`data/` 原地保留。

每次发版用私有仓库里的 `tools/publish_update.py` 覆盖式推送，所以每个分支永远只有一个提交，
仓库体积不会随版本累积。
