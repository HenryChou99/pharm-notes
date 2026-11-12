# 國考藥理筆記（MkDocs）

## 本機預覽

```bash
pip install -r requirements.txt
mkdocs serve        # 打開 http://127.0.0.1:8000 ，存檔就會自動重新整理
```

## 加筆記

所有內容在 `docs/` 底下的 `.md` 檔。每節後面都有綠色的「我的筆記」框：

```markdown
!!! mynote "我的筆記"
    在這裡寫（記得縮排 4 格）
```

其他常用框：`!!! tip`、`!!! warning`、`!!! danger`；可收合的框：`??? question "標題"`。

## 部署到 GitHub Pages

1. 在 GitHub 建立新的 repo（例如 `pharm-notes`），把整個資料夾推上去
2. repo → Settings → Pages → Source 選 **GitHub Actions**
3. 每次 push 到 `main`，`.github/workflows/deploy.yml` 會自動建置並發佈到
   `https://<你的帳號>.github.io/pharm-notes/`

或手動：`mkdocs gh-deploy`

## 新增章節

1. 在 `docs/pharm/` 新增 `xxx.md`
2. 在 `mkdocs.yml` 的 `nav:` 底下加一行
