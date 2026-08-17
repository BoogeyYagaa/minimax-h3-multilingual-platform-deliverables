<p align="right">
  <a href="./README.md"><img src="https://img.shields.io/badge/Language-English-0969da?style=for-the-badge" alt="切换到英文"></a>
  <a href="./README.zh-CN.md"><img src="https://img.shields.io/badge/%E8%AF%AD%E8%A8%80-%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87-d73a49?style=for-the-badge" alt="阅读简体中文版"></a>
</p>

# MiniMax H3 多语言平台交付物

本公开仓库包含一组 MiniMax H3 多语言文章的八个平台定制版本，以及投稿说明、合规审计、来源清单和项目审阅记录。

目前已有两篇文章在目标平台公开发布并完成页面核对。其余文件仍是编辑交付物或受平台门槛阻塞的投稿稿件，具体状态如下。

## 第三方 API 入口

如需评估统一的第三方工作流，可查看 [Affordable MiniMax H3 API](https://bestimage.ai/models/minimax/minimax-h3-text-to-video/?via=shixi88)。

**披露：** Best Image AI 是第三方服务，并非 MiniMax 官方接口。链接包含 `via=shixi88` 跟踪参数。该锚文本不代表已经核实的价格比较结论；使用前请直接核对模型可用性、控制项、实时价格、隐私政策与服务条款。

## 平台对应关系

| Locale | 文章主题 | 目标平台 | 交付目录 | 当前状态 |
|---|---|---|---|---|
| en-US | 产品发布视频 | Indie Hackers | [`minimax-h3-product-launch-indiehackers-en`](./minimax-h3-product-launch-indiehackers-en/) | 阻塞：账号尚无发帖权限 |
| es-419 | 旅行与美食视频 | Dreamwidth | [`minimax-h3-travel-journal-dreamwidth-es`](./minimax-h3-travel-journal-dreamwidth-es/) | [已发布](https://bestimage.dreamwidth.org/482.html) |
| pt-BR | 电商 UGC 视频 | Guides.co | [`minimax-h3-ugc-guide-guides-ptbr`](./minimax-h3-ugc-guide-guides-ptbr/) | `HOLD — ACCESS REQUIRED`，等待访问权限 |
| ja-JP | 动漫宣传视频 | Hatena Blog | [`minimax-h3-anime-pv-hatena-ja`](./minimax-h3-anime-pv-hatena-ja/) | 已提交博客开通申请，等待审核 |
| de-DE | SaaS 讲解视频 | DEV | [`minimax-h3-saas-explainer-dev-de`](./minimax-h3-saas-explainer-dev-de/) | `HOLD — HUMAN TECHNICAL REVIEW REQUIRED`，等待人工技术复核 |
| fr-FR | 时尚视频视觉方向 | OverBlog | [`minimax-h3-fashion-directions-overblog-fr`](./minimax-h3-fashion-directions-overblog-fr/) | [已发布](https://bestimage888.overblog.fr/7-directions-visuelles-film-mode-15-secondes) |
| zh-CN | 分镜与 API 工作流 | CSDN | [`minimax-h3-storyboard-api-csdn-zh-cn`](./minimax-h3-storyboard-api-csdn-zh-cn/) | 阻塞：发布前需要绑定微信 |
| zh-TW | 直式影片构图 | Medium | [`minimax-h3-vertical-video-medium-zh-tw`](./minimax-h3-vertical-video-medium-zh-tw/) | 阻塞：编辑器无法保存文章 |

项目记录存放在 [`minimax-h3-multilingual-review-diary`](./minimax-h3-multilingual-review-diary/) 目录。

## 每个平台包包含什么

每个平台目录包括：

- 针对目标平台改写的 Markdown 正文；
- 可供粘贴或导入的 HTML 发布版；
- 投稿填写与操作说明；
- 平台合规审计；
- 来源清单；
- 平台配图。

Medium 内容包另外包含 Word 文档和三张章节配图。

已经发布的平台目录另含 `publication-record.md`，记录经过核对的公开 URL、发布日期和页面检查结果。

## 发布前的安全门槛

- 八篇平台正文均已移除商业跟踪链接和第三方 CTA。
- Guides.co 在发布权限确认前保持暂停状态。
- DEV 文章必须完成人工技术复核后才能投稿。
- OverBlog 文章已在完成内容权利、赞助关系、广告素材和外部链接检查后发布；后续修改仍须执行同样的复核。
- 正式发布前，应再次检查平台政策、API 实时可用性、图片路径、Locale 设置和最终发布 URL。

## 独立项目声明

本仓库是独立编辑项目，不是 MiniMax 官方仓库，也不代表 MiniMax 或任何目标发布平台对其中内容提供认可或背书。
