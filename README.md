# 100ASK 桌面 AI 终端解决方案官网

面向品牌商、方案商与行业客户的静态方案官网。页面使用真实产品渲染素材，介绍 AI 对话、HDMI 视觉、USB HID 控制、OTA 运维及三档商业交付方案。

## 本地预览

本项目没有构建步骤，在仓库根目录运行：

```bash
python3 -m http.server 4173
```

然后访问 <http://127.0.0.1:4173/>。

## 项目结构

- `index.html`：首页语义结构与中文文案。
- `styles.css`：桌面、平板和手机端响应式视觉。
- `script.js`：移动导航、滚动入场与演示弹窗。
- `assets/`：真实产品透明图与场景图。
- `docs/`：可下载的方案资料。
- `.github/workflows/pages.yml`：GitHub Pages 自动部署工作流。

## 部署

推送到 `main` 分支后，GitHub Actions 会将仓库根目录发布到 GitHub Pages：

<https://dshanpi.github.io/AI-DeskTopBox/>

首次部署需在仓库的 **Settings → Pages → Build and deployment → Source** 中选择 **GitHub Actions**。

建议正式二级域名使用 `aidesktop.100ask.net`。DNS 中添加一条 CNAME：

```text
名称：aidesktop
目标：dshanpi.github.io
```

DNS 生效后，再在 GitHub Pages 设置中填写 `aidesktop.100ask.net` 并启用 HTTPS。不要将仓库名附加到 CNAME 目标中。

## 待接入内容

- 用真实 AI/IPKVM 录屏替换当前演示弹窗。
- 将 Markdown 方案资料排版为正式 PDF。
- 上线前补充备案信息、隐私政策和最终商标信息。
