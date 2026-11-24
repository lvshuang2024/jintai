# 留白 · 极简图片相册

这是一个无需后端、无需安装依赖的静态图片网站，可直接部署到 GitHub Pages。

## 本地预览
1. 解压 ZIP。
2. 双击 `index.html`，用浏览器打开。
3. 示例照片默认从 Unsplash 加载，因此首次预览需要联网。

## 替换成自己的图片
1. 把图片放进 `images` 文件夹，例如 `images/photo-01.jpg`。
2. 用记事本或 VS Code 打开 `index.html`。
3. 找到 `const photos = [`，将每一项的 `image` 地址改为本地路径，例如：
   `image: "images/photo-01.jpg"`
4. `title` 是图片标题，`category` 可填写“风景”“建筑”“日常”或自定义分类。
5. 复制照片项目即可增加更多图片；删除项目即可减少图片。
6. 保存后刷新网页。图片文件名区分大小写，路径要与实际文件一致。

## 发布到 GitHub Pages
1. 登录 https://github.com ，点击右上角 `+` → `New repository`。
2. 仓库名称填写 `photo-gallery`；选择 `Public`，点击 `Create repository`。
3. 在仓库页面点击 `Add file` → `Upload files`。
4. 将 `index.html` 和整个 `images` 文件夹里的图片上传（也可以先上传整个项目的文件）。
5. 在页面底部点击 `Commit changes`。
6. 打开仓库 `Settings` → 左侧 `Pages`。
7. 在 `Build and deployment` 下，`Source` 选择 `Deploy from a branch`。
8. `Branch` 选择 `main`，目录选择 `/ (root)`，点击 `Save`。
9. 等待一两分钟，刷新 Pages 页面，访问显示的 `https://你的用户名.github.io/photo-gallery/` 地址。

## 注意
- 首页文件必须叫 `index.html`，并放在发布目录根目录。
- 本项目纯静态，无需 Node.js、数据库或构建命令。
- 示例图片使用外部图片地址；如需长期稳定展示，建议换成自己拥有使用权的图片并上传到 `images` 文件夹。
- GitHub 仓库和 Pages 站点公开后，上传的图片也会公开。不要上传私人或敏感图片。
