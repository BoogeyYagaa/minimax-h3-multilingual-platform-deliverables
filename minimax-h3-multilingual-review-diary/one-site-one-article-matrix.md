# MiniMax H3 一站一文分配矩阵

**执行日期：** 2026年8月14日  
**项目边界：** 8 篇原始文章 × 8 个唯一网站；保留原有 8 个 Locale；另建平台发布版，不修改原文。  
**当前结果：** 8/8 个平台包已建立，线上发布数量为 0。

| Locale | 原始内容包 | 目标网站 | 平台发布包 | 平台正文 | 当前状态 |
|---|---|---|---|---|---|
| `en-US` | `minimax-h3-cinematic-product-videos/` | Indie Hackers | `minimax-h3-product-launch-indiehackers-en/` | `article.indiehackers.en-us.md` | `READY FOR MANUAL PLATFORM REVIEW` |
| `es-419` | `minimax-h3-travel-food-videos-es/` | Dreamwidth | `minimax-h3-travel-journal-dreamwidth-es/` | `article.dreamwidth.es-419.md` | `READY FOR MANUAL PLATFORM REVIEW` |
| `pt-BR` | `minimax-h3-ugc-ecommerce-videos-ptbr/` | Guides.co | `minimax-h3-ugc-guide-guides-ptbr/` | `article.guides.pt-br.md` | `HOLD — ACCESS REQUIRED` |
| `ja-JP` | `minimax-h3-anime-pv-ja/` | Hatena Blog | `minimax-h3-anime-pv-hatena-ja/` | `article.hatena.ja-jp.md` | `READY FOR MANUAL PLATFORM REVIEW` |
| `de-DE` | `minimax-h3-saas-explainer-de/` | DEV | `minimax-h3-saas-explainer-dev-de/` | `article.dev.de-de.md` | `HOLD — HUMAN TECHNICAL REVIEW REQUIRED` |
| `fr-FR` | `minimax-h3-fashion-video-fr/` | OverBlog | `minimax-h3-fashion-directions-overblog-fr/` | `article.overblog.fr-fr.md` | `READY FOR MANUAL PLATFORM REVIEW`（中风险） |
| `zh-CN` | `minimax-h3-video-storyboard-guide-zh-cn/` | CSDN | `minimax-h3-storyboard-api-csdn-zh-cn/` | `article.csdn.zh-cn.md` | `READY FOR MANUAL PLATFORM REVIEW` |
| `zh-TW` | `minimax-h3-vertical-video-guide-zh-tw/` | Medium | `minimax-h3-vertical-video-medium-zh-tw/` | `article.medium.zh-tw.md`、`article.docx` | `READY FOR MANUAL PLATFORM REVIEW` |

## 可进入人工复核的 6 个平台包

- Indie Hackers、Dreamwidth、Hatena Blog、OverBlog、CSDN、Medium。
- “可进入人工复核”不等同于已获平台批准或已经发布。
- OverBlog 仍须满足内容权利、非付费代发、无跟踪 CTA、无外部广告素材四项门槛。

## 保持暂停的 2 个平台包

- Guides.co：`HOLD — ACCESS REQUIRED`。账号权限未确认前，不计入可发布数量。
- DEV：`HOLD — HUMAN TECHNICAL REVIEW REQUIRED`。人工作者须复核技术准确性、AI 披露、内容责任与非商业推广目的。

## 查重与发布边界

- 本地交付包未发现这八个候选平台已有 MiniMax H3 专用稿。
- 这一结论只覆盖当前本地文件，不能证明远程账号从未发布；实际投稿前须人工检查账号历史和平台搜索结果。
- 八篇平台正文均不含 Best Image AI、`via=shixi88` 或商业 CTA。
- 本轮不登录平台、不创建草稿、不提交审核、不记录虚构发布 URL。

## 每个平台包的标准文件

- `article.<platform>.<locale>.md`
- `article.<platform>.<locale>.html`（独立本地预览版，内嵌响应式 CSS）
- `submission-notes.md`
- `platform-audit.md`
- `source-manifest.md`
- 平台主图；Medium 另含 Word 版和三张章节配图。

## HTML 追加交付

- 2026年8月14日为 8 个平台包各增加一份 HTML，未覆盖 Markdown、Word、审计或图片。
- HTML 使用正确的 Locale `lang` 属性、UTF-8、移动端 viewport、文章标题与交付状态元数据。
- 页面样式完全内嵌，不调用第三方 CDN；文章图片继续使用同目录相对路径。
- HTML 只是可独立打开的预览与移交格式。实际平台若过滤 `<head>`、`<style>` 或完整文档标签，应只取正文并在平台预览中人工检查。
- Guides.co 与 DEV 的 HTML 不解除原有 HOLD；线上发布数量仍为 0。
