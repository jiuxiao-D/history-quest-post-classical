# Folio AI · 深色文档工作台

在线访问（GitHub Pages）：https://jiuxiao-d.github.io/history-quest-post-classical/folio-ai/

左侧打开本地 PDF / DOCX / PPTX / TXT / Markdown 等文件；右侧设置 OpenAI-compatible Chat Completions API 后与 AI 对话。支持文档相关段落作为上下文、流式回复、拖动调整双栏、AES-GCM 加密浏览器本地 API 配置。

## 开始使用

1. 打开上方页面并点击 **API 设置**。
2. 填写你自己的 **HTTPS URL、Model 和 API Key**，选择 **自动** / **浏览器直连**。
3. 点击 **应用配置**。打开本地文档，即可在右侧聊天。
4. 如果要跨页面保存设置，可使用 **加密保存**，并设置独立于 API Key 的强密码。

## GitHub Pages 的限制

GitHub Pages 是 **静态托管**：无法运行 Node.js 服务端代理。API 必须允许来自网页的 CORS 调用；如果服务商禁止浏览器跨域，即使 URL/Key 正确也会失败。

如遇 CORS，使用 ChatGPT 提供的 **Folio_AI_Dark_Project.zip** 在本地执行 `node server.mjs`，并选择本地代理。

**安全提示：** 不要把 API Key 或私有文档提交到公开仓库。网页不会向 GitHub 上传所选本地文件；但如果勾选“提问时附加当前文档的相关内容”，相关文字会发送给你配置的 API 服务商。加密保存保护浏览器静态存储，不保护设备遭受恶意扩展或脚本攻击时的密钥。

网页使用 CDN 加载 PDF.js 以提取 PDF 文字；扫描版 PDF 和图片不具备 OCR。
