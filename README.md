# PPT Tools — Excel 转 PPT 表格

把 Excel 表格转成简约风格的 HTML 表格，一键导出为图片，直接粘贴到 PPT。

无需安装，单文件纯前端，浏览器打开即用。

## 在线使用

直接下载 [`index.html`](./index.html) 并在浏览器中打开即可。也可以把它部署到任意静态托管（GitHub Pages / Vercel / Netlify）。

## 功能

- 支持 `.xlsx` / `.xls` / `.csv`，可拖拽或点击上传
- 多工作表自动识别，提供切换标签
- 5 种 PPT 友好的表格风格：
  - **极简 Minimal** — 顶/底细线，行间淡色分隔
  - **条纹 Banded** — 轻微隔行底色
  - **刊物 Editorial** — 衬线体表头，宽行距，适合长文表格
  - **主色 Accent** — 单色表头，可自选颜色
  - **卡片 Card** — 圆角卡片＋柔和阴影
- 可调字号 / 行高 / 表头模式 / 表格标题
- 数值列自动右对齐，使用等宽数字（tabular-nums）
- 导出 PNG 图片，默认 2× 高清，直接粘贴 PPT 不模糊

## 使用步骤

1. 浏览器打开 `index.html`
2. 拖拽或点击上传 Excel 文件
3. 在工具栏选择样式、调整字号/行高/标题
4. 多工作表可在顶部标签切换
5. 点击 **下载为图片** 得到 PNG，粘贴到 PPT 即可

## 技术栈

- [SheetJS (xlsx)](https://github.com/SheetJS/sheetjs) — Excel 解析
- [html2canvas](https://github.com/niklasvh/html2canvas) — DOM 转图片
- 纯 HTML + CSS + JS，无构建步骤，无后端依赖

依赖通过 jsDelivr CDN 加载。如需完全离线使用，把两个脚本下载到本地，替换 `<script src>` 路径即可。

## 离线部署

```bash
# 直接静态托管
python3 -m http.server 8000
# 然后访问 http://localhost:8000
```

或部署到任何静态托管平台。

## 浏览器兼容

- Chrome / Edge / Safari / Firefox 现代版本
- 需要支持 ES2017+ 与 FileReader API

## License

MIT
