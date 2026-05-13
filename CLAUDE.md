# localwipe
AI 去水印工具，100% 本地处理，图片不上传服务器。面向海外用户的全英文静态站。

## 技术栈
- 纯前端静态站，所有代码内联在 index.html
- Tailwind CSS v3 (CDN)
- Font Awesome 6 Free (CDN)
- Canvas API（画笔 + 图像修复）
- JSZip (CDN)
- Google Fonts: Inter

## 部署
GitHub + Cloudflare Pages 自动部署。推送到 GitHub main 分支即自动更新线上。

## 约定
- 所有界面文字必须是英文
- 所有 CSS/JS 内联在 index.html，不拆分文件
- 广告位用占位符，GA4 用占位符

## 验证
```bash
# 直接浏览器打开即可验证
start index.html
```
