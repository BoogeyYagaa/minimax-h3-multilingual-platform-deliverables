# Medium 平台合规审计

## 结论

**READY FOR MANUAL PLATFORM REVIEW**。正文已按 Medium 的编辑型长文重构，保留繁中 Locale，删除商业 CTA 与跟踪参数。当前状态不等同于发布批准；发布者仍须在账号内完成政策与预览检查。

## 已完成检查

- 标题与开头以观点和读者问题切入，未把 MiniMax H3 写成广告入口。
- 正文为 4 个编辑章节，每个章节末均配置一张图片及 AI 生成说明。
- 前两段内明确披露 AI 协助；所有生成图片均逐张披露。
- MiniMax H3 的输入模态、768P/2K、4—15 秒与 `ratio` 模式差异均依据 2026 年 8 月 14 日可见的官方文件复核。
- 文生、首尾幀图生、多模态参考生成未被写成相同的 9:16 设置流程。
- 未使用 Best Image AI、`via=shixi88`、联盟链接、价格主张或商业 CTA。
- 未启用付费墙，也未设置不存在的 canonical URL。
- 台灣用语使用 `影片、直式、畫面、介面、連結、專案` 等自然表达。
- `article.docx` 已在 Pages 中打开并导出为 6 页 PDF；逐页视觉检查未发现中文缺字、文字重叠、图片裁切或标题层级异常。LibreOffice 在本机缺少完整 CJK 渲染支持，因此不作为本轮视觉验收依据。
- 本地交付包未发现 Medium 的 MiniMax H3 专用稿；这不代表远程账号从未发布，发布前须人工检查账号历史。

## 发布门槛

1. 人工复查 Medium 当日的 AI 内容政策与平台规则。
2. 确认账号中的 AI 披露、图片说明和标签与本文一致。
3. 上传图片并在预览中检查移动端裁切、替代文字和章节顺序。
4. 如已有正式首发 URL，再判断是否设置 canonical；不得把本地文件路径当 URL。
5. 确认最终文章没有付费墙、跟踪 CTA 或新增商业推广链接。

## 依据

- [Medium AI 内容政策](https://help.medium.com/hc/en-us/articles/22576852947223-Artificial-Intelligence-AI-content-policy)
- [Medium 平台规则](https://help.medium.com/hc/en-us/articles/213477928-Medium-Rules)
- [MiniMax 影片生成文件](https://platform.minimaxi.com/docs/guides/video-generation)
- [MiniMax v2 建立影片生成任务](https://platform.minimaxi.com/docs/api-reference/video-generation-v2-create)
