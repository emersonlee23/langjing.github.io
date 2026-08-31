# 朗境酒庄官网 · Chateau Langjing Website

> 中国·云南·德钦·梅里产区  ·  一个生长在雪域高原上的精品酒庄
> 官方网站采用素描极简灰白风格设计，配合 Noto Serif SC + Cormorant Garamond 衬线字体，体现雪域高原葡萄酒的克制与高级感。

## 目录结构

```
朗境网站/
├── index.html              主页（单文件 HTML，含中英双语）
├── images/                 图片资源目录（与 index.html 平级）
│   ├── hero-snowpeak.jpg              Hero 大图（雪山云海）
│   ├── hero-vineyard.jpg              Hero 备选（葡萄园主视觉，备而未用）
│   ├── terroir-misty-hills.jpg        一·秘境之酿 配图
│   ├── terroir-vineyard-view.jpg      二·风土 全景配图（pull figure）
│   ├── terroir-grape.jpg              二·风土 葡萄特写（duo）
│   ├── terroir-vineyard-cultivator.jpg 二·风土 葡萄园人物（duo）
│   ├── culture-village-terrace.jpg    三·藏地人文 村落梯田（pull figure）
│   ├── culture-stupa-snowpeak.jpg     三·藏地人文 白塔雪山（duo）
│   ├── culture-tibetan-child.jpg      三·藏地人文 藏族小孩（duo）
│   ├── quality-detail.png             四·品质追求 工艺图
│   ├── coda-sunset-meili.jpg          五·结语 日照金山
│   └── brand-extra.jpg                备用品牌图（备而未用）
└── README.md               本文件
```

## 上传到 GitHub 仓库

### 方案一：直接 push 到新仓库

1. 在 GitHub 创建新仓库（如 `chateau-langjing-website`）
2. 在本目录初始化 git：
   ```bash
   cd 朗境网站/
   git init
   git add .
   git commit -m "feat: initial website with pencil-sketch minimalist design"
   git branch -M main
   git remote add origin git@github.com:YOUR_NAME/chateau-langjing-website.git
   git push -u origin main
   ```

3. **打开 GitHub Pages**：仓库 Settings → Pages → Source 选 `main` branch, `/ (root)` → Save
4. 几分钟后即可访问 `https://YOUR_NAME.github.io/chateau-langjing-website/`

### 方案二：用 GitHub 网页上传

1. 在 GitHub 创建新仓库
2. 依次点击 `Add file → Upload files`
3. **重要**：先上传整个 `images/` 文件夹（保持子目录结构）
4. 再上传 `index.html`
5. 启用 GitHub Pages（同上方案一第 3 步）

### ⚠️ 注意事项

- **保持 `images/` 子目录结构**：HTML 内的 `<img src="images/xxx.jpg">` 是相对路径，如果把图片平铺到根目录，需要批量替换路径
- **不要上传中文/特殊字符文件名**：本项目已全部清洗为英文小写（如 `IMG_1735.jpeg` → `hero-snowpeak.jpg`）
- **CJK 字体注音**：网页使用 Google Fonts（CDN 加载），无需本地字体文件
- **图片体积**：当前总图片 ~50 MB，可考虑后期用 imageoptim / squoosh 压缩到 10-20 MB 再上传

## 设计风格说明

- **视觉风格**：素描极简灰白（Pencil Sketch Minimalist Grey-White）
- **主色板**：暖白 `#F8F6F2` · 中性灰 `#888-#C0C0C0` · 深灰 `#1B1A18` · 金色点缀 `#A88A55`
- **字体方案**：思源宋体 (Noto Serif SC) + Cormorant Garamond 衬线字体
- **节奏**：单页长滚动，章节间由手绘分隔，章节内 fade-in 揭示
- **语言切换**：顶栏 ZH/EN 切换按钮，状态本地存储

## 浏览器兼容性

- 支持现代 Chrome / Safari / Edge / Firefox
- 移动端响应式适配（< 900px 自适应）
- 使用 CSS 变量、`backdrop-filter`、`IntersectionObserver` 等现代特性
