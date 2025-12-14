# 个人主页说明

这是一个基于 GitHub Pages 的个人主页项目，页面使用简单的静态 HTML 和 CSS 构建，并加入了雪花动画效果和渐显动画。主页展示了个人简介、技能、教育经历、工作经历等信息，其中敏感信息（联系方式）和完整的项目经历经过 Base64 加密处理。

# 如何查看加密内容

- 主页加载后，联系方式和项目经历默认处于加密状态。页面底部会显示一个验证输入框。
- 输入绑定的 手机号（例如 xxxxxxxx）或 邮箱地址（例如 xxxxxxxxxxxx）并点击“验证并解密”按钮，页面会自动解密并显示隐藏内容。
- 如果需要更换验证方式或修改预设的手机号/邮箱，可以编辑 index.html 中 JavaScript 部分的 expectedPhone 和 expectedEmail 变量。

# 使用方法

## 本地预览：

将仓库克隆到本地：

git clone https://github.com/<your-username>/<your-repo>.git


双击打开 index.html 即可在浏览器中预览页面效果。

## 部署到 GitHub Pages：

将仓库推送到 GitHub，确保分支为 main 或 gh-pages，并在仓库设置中启用 GitHub Pages。

GitHub Pages 启用后，稍等片刻即可通过 https://<your-username>.github.io/<your-repo>/ 访问个人主页。

### 自定义内容：

修改个人信息、技能列表等内容可以直接编辑 index.html 对应部分。

加密的联系方式和项目经历位于 index.html 的 JavaScript 中，通过修改 sensitiveInfoEncoded 和 projectsEncoded 的 Base64 字符串可以替换为新的内容。编码方式可使用在线工具或 btoa 在浏览器控制台中生成。

其他注意事项：

本项目为纯前端静态页，无需服务器支持。

如果不需要加密功能，可直接在页面中显示完整内容，将验证逻辑和相关变量删除即可。
