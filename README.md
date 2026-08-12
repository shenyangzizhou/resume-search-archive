# 简历搜索招聘指令归档 - 公网部署包

本目录是简历搜索招聘指令归档的静态站点部署包，`index.html` 由
`../update_archive.py` 自动生成。

## 部署到 GitHub Pages

1. 在 GitHub 新建一个公开仓库（例如 `resume-search-archive`）。
2. 将本目录内容推送到仓库 `main` 分支：

```powershell
cd "C:\Users\申阳\Documents\recruiting- copilot\recruiting\resume_search\archives\site-deploy"
git init
git add .
git commit -m "init archive site"
git branch -M main
git remote add origin https://github.com/<你的用户名>/resume-search-archive.git
git push -u origin main
```

3. 推送后 GitHub Actions 会自动执行 `.github/workflows/deploy-pages.yml`，
   发布后访问地址为：

```text
https://<你的用户名>.github.io/resume-search-archive/
```

后续每次运行 `update_archive.py` 会重新生成 `index.html`，提交并推送即可更新。
