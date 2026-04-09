# flatpak-dbeaver automation

这个仓库通过 GitHub Actions 自动同步 `flathub/io.dbeaver.DBeaverCommunity` 的内容，并在有更新时自动提交、推送并创建 GitHub Release。

## 自动化行为

- 每 6 小时同步一次上游仓库。
- 也支持手动触发（`workflow_dispatch`）。
- 如果检测到内容变化：
  - 自动提交到当前分支。
  - 自动推送到本仓库。
  - 自动创建一个新的 GitHub Release。

工作流文件：`.github/workflows/sync-flathub-dbeaver.yml`
