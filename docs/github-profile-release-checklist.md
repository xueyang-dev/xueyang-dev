# Folith 发布前 GitHub Profile 清单

审计日期：2026-10-01。事实来源为 GitHub 公开资料、默认分支 README、元数据、提交和代码；不以本机 Folith 未提交改动代表已发布能力。

## GitHub Profile Audit

### P0 — 发布前必须解决

1. **旗舰项目缺席**
   - 当前证据：旧 Profile 两种语言都以 HanClassStudio、localize-anything、TransPraxis/MTI 为代表项目，没有 Folith；Current Work 仍是教育内核、私有本地化项目和 macOS 探索。
   - 问题：首页无法识别当前主要产品。
   - 发布影响：访客短时间内无法理解 Folith 与作者的关系。
   - 修改方案：第一屏为姓名、个人定位、Building/Folith、问题与工作流说明及 Repository/Releases 两个入口。
2. **公开作品与可见性不匹配**
   - 当前证据：localize-anything 已 private；8 个公开仓库中只有 Folith、HanClassStudio、TransPraxis、Profile 不是 fork。
   - 问题：私有项目无法面向陌生访客展示；前身与 Folith 并列会重复产品叙事。
   - 发布影响：无效公开入口和两个等权品牌降低可信度与点击集中度。
   - 修改方案：只展示 Folith 和 HanClassStudio；质量优先，暂无第三个独立公开原创作品可推荐。
3. **TransPraxis 未指明演进关系**
   - 当前证据：[Folith 初始化提交](https://github.com/xueyang-dev/Folith/commit/e8717f2d60f7c8358e72cef7f8587891c7399df3) 明确为 `bootstrap FolioThread from TransPraxis v0.4 baseline`；[Folith 品牌发布](https://github.com/xueyang-dev/Folith/commit/f05219b27dac2c167cd8668b9635fc4851a5345f)；[pyproject.toml](https://github.com/xueyang-dev/Folith/blob/main/pyproject.toml) 保留 transpraxis 命令兼容入口。
   - 问题：旧 README 描述类似能力但没有后继项目入口。
   - 发布影响：旧链接可能使用户误入历史产品。
   - 修改方案：旧 README 最顶部加入中英文迁移说明，正文保留历史记录。

### P1 — 推荐解决

1. **双语信息漂移**
   - 当前证据：中文写 TransPraxis，英文链接 MTI-Tool-for-Translation-Practice；GitHub 当前将 MTI 旧 URL 重定向到 TransPraxis，并非独立现存仓库。
   - 问题：名称过时且语言版本不一致。
   - 发布影响：不同语言访客得到不同项目身份。
   - 修改方案：两份 README 同步结构、作品、当前工作、技术与联系方式，移除旧入口。
2. **Folith 产品定位冲突**
   - 当前证据：description 是 `Folith · 译页 — Agentic Localization Workspace / Agentic 本地化工作台`；README 首屏、图像 alt、[品牌规范](https://github.com/xueyang-dev/Folith/blob/main/docs/brand.md)、[brand.py](https://github.com/xueyang-dev/Folith/blob/main/transpraxis/brand.py) 和包描述是 `Agentic Translation Workspace`。
   - 问题：[2026-09-22 的品牌提交](https://github.com/xueyang-dev/Folith/commit/0104dc2de10bfa69324a94d62ba2fe0ca2ffd01d) 明确主动采用过 Translation；当前发布要求则指定 Localization。这是品牌决策发生变化后尚待同步，不宜假装只是一处拼写错误。
   - 发布影响：Profile、仓库摘要与产品 README 使用不同定位。
   - 修改方案：本次 Profile 使用 `Folith · 译页 — Agentic Localization Workspace / 智能体本地化工作台`。后续单独同步产品 README 开场、品牌规范、正式素材与包描述。CAT 可作为功能语境，AI translation 可作为能力描述，不应再作为并列主定位。
   - 本次不改 Folith 产品 README、素材或功能代码。
3. **个人资料与技术信息不足**
   - 当前证据：公开 Bio、Website、社交链接为空；没有 Pins；Status 为 🎯 Focusing。旧技术列表有 Kotlin/Swift，但当前代表项目不支持将其列为主要技术。
   - 问题：侧栏没有当前产品线索，技术列表与作品脱节。
   - 发布影响：作者识别和产品入口不清晰。
   - 修改方案：手工填写下方 Bio、Pins；README 说明 Python 在两个项目中的核心用途，补充有代码依据的前端技术。

### P2 — 可后续处理

1. **社交预览和主页地址**
   - 当前证据：Folith `usesCustomOpenGraphImage=false`，homepage 为空；topics 已覆盖主要定位。
   - 问题：默认分享图缺少专属品牌辨识；未确认独立产品站点。
   - 发布影响：外部分享吸引力有限，但 homepage 为空不是功能缺陷。
   - 修改方案：上传统一定位的 social preview；不虚构官网。现有 topics 保留。
2. **历史安装入口**
   - 当前证据：TransPraxis README 推荐 v0.4.0 wheel，但该公开 Release 当前没有附件；v0.3.0 和 v0.2.1 有附件。Folith v0.4.0 实际有 foliothread wheel 与 sdist。
   - 问题：旧文档安装建议无法按描述完成。
   - 发布影响：从历史项目进入的用户可能卡在下载。
   - 修改方案：迁移说明引导新用户至 Folith，旧正文作为历史记录保留；本次不修改任何 Release。

## 公开仓库盘点

| 仓库 | 公开 description | Topics | Fork | 处理 |
| --- | --- | --- | --- | --- |
| Folith | Folith · 译页 — Agentic Localization Workspace / Agentic 本地化工作台 | agentic-localization, document-localization, localization, python, streamlit, translation, translation-memory | 否 | 旗舰、第一 Pin |
| HanClassStudio | 专门用于国际中文教育课件制作的开源skills和workflow | 无 | 否 | 第二作品、第二 Pin |
| TransPraxis | TransPraxis / 译践 — AI辅助翻译实践、术语管理、交付和学术写作工作空间。 | 无 | 否 | 前身，迁移入口，不与 Folith 等权 |
| xueyang-dev | 空 | 无 | 否 | Profile 仓库，不作为产品 |
| claudian | An Obsidian plugin that embeds Claude Code/Codex as an AI collaborator in your vault | 无 | 是 | 不列为原创代表作 |
| ebook2audiobook_GPTSOVITS_added | Generate audiobooks from e-books, voice cloning & 1158+ languages! | 无 | 是 | 不列为原创代表作 |
| opencodex | Universal provider proxy for OpenAI Codex & Claude Code — use any LLM (Claude, Gemini, Grok, DeepSeek, Ollama…) with Codex CLI, App, SDK, and Claude Code | 无 | 是 | 不列为原创代表作 |
| vorssaint-utils | Free and open-source macOS menu bar toolkit. | 无 | 是 | 不列为原创代表作 |

以上公开仓库均未 archived。localize-anything 已私有，移除 Profile 入口；无需披露更多私有项目细节。

## 文案事实依据

- Folith 的术语候选与锁定、翻译记忆语言隔离、人工确认和交付审校门禁可在默认分支的 [terminology.py](https://github.com/xueyang-dev/Folith/blob/main/transpraxis/terminology.py)、[translation_memory.py](https://github.com/xueyang-dev/Folith/blob/main/transpraxis/translation_memory.py)、[delivery.py](https://github.com/xueyang-dev/Folith/blob/main/transpraxis/delivery.py) 确认。Profile 只概述工作流，不承诺零错误、秒级恢复或自动保证质量。
- Folith 技术来自 [requirements.txt](https://github.com/xueyang-dev/Folith/blob/main/requirements.txt)：Python、Streamlit、PyMuPDF、python-docx。
- HanClassStudio 技术来自 [API pyproject.toml](https://github.com/xueyang-dev/HanClassStudio/blob/main/apps/api/pyproject.toml) 和 [Web package.json](https://github.com/xueyang-dev/HanClassStudio/blob/main/apps/web/package.json)：Python/FastAPI、TypeScript/React/Vite。HTML/PPTX 输出有 README 与 pipeline/render 实现支持。
- HanClassStudio 最新默认分支提交为 2026-07-27（仓库 pushed_at 为 2026-07-30）；README 明示内部技术验证完成、真实教学验证尚未开始。不能凭 push 时间声称正在持续维护，因此未列入 Current Work。
- Folith 存在真实仓库内文档与界面截图，但未确认独立文档站。Profile 控制为 Repository/Releases 两个 CTA；截图可在产品 README 查看。

## Manual GitHub Settings

以下仅建议，未通过 API 或 UI 自动修改。

### Display Name

当前：`XUEYang`。默认建议保留有辨识度的 `XUEYang`，Profile H1 为 `XUEYang / 薛扬`。

如果希望中英文访客在侧栏直接识别姓名，推荐 `Xue Yang / 薛扬`；纯英文备选为 `Xue Yang`，也与 Folith 包作者名一致。无需为形式统一强制改名。

### Bio

当前公开 Bio 为空。候选：

1. **推荐：** `Building Folith · 译页 — an agentic localization workspace for long-form translation.`
2. `AI-native tools for translation, localization, and language workflows. Building Folith · 译页.`
3. `构建面向真实工作流的 AI 原生工具。正在做 Folith · 译页：长文档翻译与本地化工作台。`

### Status

当前：`🎯 Focusing`。

建议：`Building Folith · 译页`。可不设置到期时间；避免“launching this week”等迅速过期文案。无需 emoji。

### Pinned Repositories

当前没有 Pins。推荐顺序：

1. **Folith** — 旗舰。
2. **HanClassStudio** — 教育方向原创作品。

暂不补满六格。TransPraxis 为历史前身，不与 Folith 并列；fork 不占核心位置。将来有新的公开原创作品，再补充第三项。

### Website / Social links

当前 Website 与社交链接均为空，未确认个人网站或产品官网。

可填写确实存在的 [Folith 仓库](https://github.com/xueyang-dev/Folith)，也可保持 Website 为空。未提供社交账号，不建议添加；不公开私人联系方式。

### 联系方式

Folith 和 HanClassStudio 均启用 Issues，均未启用 Discussions。Profile 仅使用 Issues；未启用前不添加 Discussions CTA。

## Folith Repo Metadata Audit

- **Description：**现有英文定位正确，可将中文规范为 `Folith · 译页 — Agentic Localization Workspace / 智能体本地化工作台`。
- **Topics：**现有七项合理且有仓库依据，无需为了数量增加泛 AI 标签。后续可考虑 `terminology-management`，但不是发布阻断项。
- **Homepage：**空；没有独立官网证据，不建议占位地址。
- **Social preview：**GitHub 默认生成图。建议到 Settings → General → Social preview 上传简洁图片，包含品牌名、统一副标题和真实界面；本次不生成或上传。
- **README title：**`Folith · 译页` 正确。
- **README opening：**Translation 与 Localization 差异见 P1。开场中的“都能保持”“杜绝”等绝对质量表述超出仅凭代码能证明的范围；建议后续改为“支持上下文与术语一致性检查”“提供审校和可追溯交付”。本次不进行产品 README 重写。
- **旧名称：**`foliothread` 发布包名、`transpraxis` 模块与 CLI 兼容入口是明确保留的技术边界，不应为清理品牌而直接更名。公开叙事使用 Folith；历史标识允许出现在兼容说明中。

## TransPraxis 后续处理

- **推荐当前方案：**保留仓库与历史 README，顶部重定向读者至 Folith；以 Folith 作为后续开发入口。
- **Archive：**可在迁移说明合并、确认没有独立维护需求及待处理问题后考虑。归档会限制后续交流，当前无需立即归档。本次不执行。
- **保留 Releases：**建议保留，维持历史版本可用性；不要删除、改写或重新发布旧版本。
- **Description：**可手工改为 `Legacy translation-practice workspace; continued development in Folith · 译页.`，与迁移说明一致。
- **Redirect README：**采用说明块而不是替换整份文档，既明确新入口，也保存历史。

## 发布与核对

- [ ] 合并 Profile 修改，使默认分支 README 在个人主页展示。
- [ ] 合并 TransPraxis 迁移说明。
- [ ] 手工选择 Display Name、Bio、Status 与 Pins。
- [ ] 后续同步 Folith Localization 定位的 README、品牌文案和素材。
- [ ] 默认分支合并后，从未登录视角检查中英文切换、首屏与 Pins。

两份 Profile 使用相同信息架构与项目集合，修改其中一份时同步另一份。不引入 README 生成框架。

## Final Verification

- 已核对：两份 Profile 的标题层级与链接集合相同，Featured Work 都只有 Folith 和 HanClassStudio；Current Work 仅 Folith。
- 已核对：新增 README 与清单链接中的公开仓库、源码、提交、Releases 和 Issues 可通过 GitHub API 访问；语言切换目标文件存在。
- 已核对：Profile 不含 MTI 旧名、TransPraxis 主项目入口、私有 localize-anything、fork 作品、Kotlin/Swift 或无效 Discussions CTA。
- 已核对：GitHub Markdown API 成功渲染两份 Profile 和 TransPraxis 迁移说明；标题/段落与顶部引用块正常，无模板图表或徽章墙。
- 已核对：TransPraxis 历史正文逐字保留，仅新增迁移说明；未更改 Release、归档状态、Folith 功能代码或本机已有改动。
- 尚未验证：合并后的公开个人主页在不同设备上的实际首屏高度、GitHub UI 设置和社交预览。Markdown 渲染通过不代表个人设置已生效。
