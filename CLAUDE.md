# corplink-rs

飞连 (FeiLian) VPN 客户端的 Rust 重实现，fork 自 [PinkD/corplink-rs](https://github.com/PinkD/corplink-rs)。

## 远程仓库

| 远程 | URL | 用途 |
|------|-----|------|
| `origin` | `git@github.com:Ben8368/corplink-rs` | 推送定制提交 |
| `upstream` | `https://github.com/PinkD/corplink-rs` | 拉取上游更新 |

## Rebase 工作流（约束）

每次同步上游必须使用 rebase，保持定制提交在历史顶部：

```
git fetch upstream
git rebase upstream/master
git push origin master --force-with-lease
```

冲突时手动解决后 `git add <file> && git rebase --continue`，放弃用 `git rebase --abort`。

**禁止** `git merge upstream/master`，禁止直接 push 到 upstream。
