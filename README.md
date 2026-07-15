# 豆包视频去水印 · 隐私政策页

本仓库托管浏览器扩展 **「豆包视频去水印」**（支持 Chrome 网上应用商店与 Microsoft Edge 应用商店上架）的**隐私政策静态网站**。

- 用途：作为扩展上架表单中「隐私政策网址」的公开页面。
- 内容：中英双语，声明扩展**不收集任何用户个人数据**、无远程代码、权限仅服务于单一用途（无水印视频/原图解析提取）。
- 联系邮箱：aigood1024@gmail.com

## 线上地址

https://hope0719.github.io/doubao-watermark-privacy/

由 GitHub Pages 自动从 `main` 分支根目录发布。

## 本地预览

项目是单个静态文件 `index.html`，无需构建。两种方式任选其一：

1. **直接打开**：双击 `index.html` 用浏览器打开即可（中/EN 切换、localStorage 记忆均正常）。
2. **本地服务器**（更接近线上环境）：
   ```bash
   python3 -m http.server 8080
   # 然后浏览器访问 http://localhost:8080/
   ```

## 结构

```
index.html        # 隐私政策单页（内嵌 CSS + JS，含中/EN 切换）
.nojekyll         # 关闭 GitHub Pages 的 Jekyll 处理
```

## 修改与发布

直接编辑 `index.html`，提交并推送到 `main` 分支，GitHub Pages 会在数十秒内自动更新：

```bash
git add index.html
git commit -m "update privacy policy"
git push origin main
```

> 注意：若处于 Clash 等代理环境且 `HTTPS_PROXY` 指向动态端口，git 推送可能报 HTTP/2 隧道错误，可将本仓库 git 代理固定为 Clash 的稳定 mixed 端口：
> `git config http.proxy socks5://127.0.0.1:7890`
