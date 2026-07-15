# 双溪村宣传网站

安徽省桐城市双溪村官方宣传网站 —— 龙眠山下的茶香古村。

## 技术栈

- 纯 HTML + CSS + JavaScript
- 无需构建工具，无需服务端
- 响应式设计，兼容手机/平板/电脑

## 在 Gitee Pages 上部署

### 方法一：直接上传

1. 登录 [Gitee](https://gitee.com)，新建仓库（如 `shuangxi-village`）
2. 将本目录下所有文件上传到仓库
3. 进入仓库 → **服务** → **Gitee Pages**
4. 开启 Pages 服务，部署分支选择 `master`，部署目录留空
5. 等待部署完成后，访问生成的 `.gitee.io` 域名即可

### 方法二：通过 Git 推送

```bash
cd shuangxi_web
git init
git add .
git commit -m "双溪村宣传网站"
git remote add origin https://gitee.com/你的用户名/仓库名.git
git push -u origin master
```

然后在仓库设置中开启 Gitee Pages。

## 替换图片指南

网站中所有需要替换图片的位置都已标注 `🖼 替换为...` 的提示文字。你需要准备以下图片（推荐 JPG 格式，大小不超过 500KB）：

| 位置 | 建议文件名 | 建议尺寸 | 说明 |
|------|-----------|---------|------|
| 首屏轮播图1 | hero1.jpg | 1920×1080 | 茶园全景 |
| 首屏轮播图2 | hero2.jpg | 1920×1080 | 文和园古建 |
| 首屏轮播图3 | hero3.jpg | 1920×1080 | 龙眠山溪流 |
| 首屏轮播图4 | hero4.jpg | 1920×1080 | 乡村诗会 |
| 走进双溪 | about-village.jpg | 800×600 | 村庄全景 |
| 茶韵双溪·茶叶 | tea-xiaohua.jpg | 600×400 | 桐城小花茶 |
| 茶韵双溪·茶园 | tea-garden.jpg | 600×400 | 茶园风光 |
| 茶韵双溪·文化馆 | tea-culture.jpg | 600×400 | 茶文化馆 |
| 文和园 | wenheyuan.jpg | 400×400 | 文和园照片 |
| 六尺巷 | liuchixiang.jpg | 400×400 | 六尺巷文化 |
| 摩崖石刻 | moya-shike.jpg | 400×400 | 摩崖石刻 |
| 龙眠山庄 | longmian-shanzhuang.jpg | 400×400 | 山庄遗址 |
| 农家菜 | food.jpg | 600×400 | 美食照片 |
| 民宿 | minsu.jpg | 600×400 | 民宿照片 |
| 伴手礼 | gifts.jpg | 600×400 | 特产照片 |
| 美丽乡村1-4 | village-new1~4.jpg | 600×400 | 建设成果 |
| 文化活动1-4 | culture1~4.jpg | 400×400 | 乡风文明活动 |

### 替换方法

1. 将准备好的 JPG 图片放入 `images/` 文件夹
2. 在 `index.html` 中搜索 `🖼` 找到标注位置
3. 将对应的背景图或图片标签替换为你的图片路径

例如，替换首屏轮播图：

```html
<!-- 替换前 -->
<div class="hero-slide active" style="background-image: url('');">

<!-- 替换后 -->
<div class="hero-slide active" style="background-image: url('images/hero1.jpg');">
```

替换后删除 `<span class="img-replace-hint">...</span>` 提示文字即可。

## 自定义内容

- 联系方式：搜索 `XXXX` 替换为实际电话号码
- 统计数据：搜索 `data-target` 修改数值
- 文字内容：直接修改 HTML 中的对应文字

## 颜色主题

- 茶绿主色：`#5B8C5A`
- 水墨灰：`#3C3C3C`
- 金色点缀：`#C4944A`

可在 CSS 的 `:root` 变量中统一修改。
