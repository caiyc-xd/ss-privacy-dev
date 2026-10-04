# ss-privacy-dev —— 开发中的站点（在途）

**这是"开发中版本"的站点**，用于避免：App 商店里用户能下载到的版本 ↔ 站点文案不一致。

| 站点 | 仓库 | Pages 源分支 | 用途 |
|---|---|---|---|
| 生产 | `caiyc-xd/ss-privacy` | `gh-pages` | Connect 里填的 Support / Privacy / Marketing URL；内容必须与**已上架版本**一致 |
| 在途（本仓库） | `caiyc-xd/ss-privacy-dev` | `main` | 正在开发的版本；可以随时更新，不影响真实用户 |

## 谁生成这些页面

主工程仓库 `ScoreStudio` 的 `Tools/Pages/build.py`（正文来源 `AppStore/Privacy-Policy*.md`
与 build.py 里的内嵌 markdown）。**不要手改本仓库的 HTML**。

```bash
# 在主工程里
python3 Tools/Pages/build.py
bash Tools/Pages/deploy.sh --dev     # 部署到本仓库（在途）
bash Tools/Pages/deploy.sh --prod    # 部署到生产仓库（未提审/未上架前一般不要跑）
```

## 站点地址

- 在途：`https://caiyc-xd.github.io/ss-privacy-dev/`
- 生产：`https://caiyc-xd.github.io/ss-privacy/`
