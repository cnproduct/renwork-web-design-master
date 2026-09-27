# 来源、边界与修订依据

核验日期：2026-09-27。以下是参考入口，不代表上游背书，也不作“最热门/最权威”的排名声明。链接可能随上游重组变化。

本仓库是围绕用户提供的排版与布局需求独立编写的操作规范，不打包上游 SKILL 文件、字体或图片。MIT 适用于本仓库原创内容；使用第三方资源时须另查其许可和署名要求。

## 已核实的上游 Skill

| 来源 | 精确入口 | 参考范围 |
|---|---|---|
| Anthropic | [frontend-design](https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md) | 依据内容与品牌做视觉判断，避免无目的的模板化表现 |
| wondelai | [web-typography](https://github.com/wondelai/skills/blob/main/web-typography/SKILL.md) | 字体的阅读角色、实现与响应式排版 |
| davepoon | [typography-selector](https://github.com/davepoon/buildwithclaude/blob/main/plugins/frontend-design-pro/skills/typography-selector/SKILL.md) | 字体选择、角色配对与前端应用 |
| Microsoft | [web-design-reviewer](https://github.com/microsoft/GitHubCopilot_Customized/blob/main/.github/skills/web-design-reviewer/SKILL.md) | 基于实际页面的视觉审查与问题修复 |

不继承其中所有偏好或数值；可用性由当前项目、用户需求和实际测试判断。

## 技术与可访问性依据

- [W3C：文字对比度](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html)：普通/大文字门槛、相对亮度与不取整判断。
- [W3C：重排](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html)：窄视口与二维内容的区分。
- [W3C：目标尺寸](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html)：24px 最小尺寸、间距及适用例外。
- [W3C：文字间距](https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html)：用户覆盖间距后不能损失内容或功能。
- [W3C：非文字对比](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html)：必要控件识别与图形信息。
- [MDN：clamp()](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/clamp)：边界与首选值语法。
- [MDN：容器查询](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Containment/Container_queries)：查询容器及组件上下文。
- [MDN：font-display](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@font-face/font-display)：字体加载时的显示策略。

W3C Understanding 页面是对标准的解释；完整合规判断须同时考虑适用规范及整个页面。自动扫描或本工具的单一数值通过不能代替完整判断。

## 对用户原稿的具体修订

| 原稿倾向 | 本 Skill 的处理 |
|---|---|
| 禁用常见/系统字体 | 依据品牌、语言、性能与可读性选择，允许有理由地使用 |
| 所有字号严格沿用统一比例 | 提供角色字阶，允许视觉修正；准确区分经验值与标准 |
| clamp 的 min/max 就是指定视口端点 | 提供可运行插值公式，明确根字号假设与缩放检查 |
| 65ch 作为所有语言的统一行长 | 区分拉丁与中文实际字形，说明 ch 不是字符计数 |
| 灰色不可用于有色背景 | 实测亮度对比，不把色相当作可访问性判据 |
| 容器查询始终优先 | 依据组件复用或整页结构分别选择容器/媒体查询 |
| 装饰禁令替代审美判断 | 优先用户品牌与内容目的，并保留可验证的质量底线 |
| 阅读生理数字作为普遍定律 | 不沿用未经当前任务核实的普遍性论断 |

另外加入中英文 fallback、长文本与 RTL 压力测试、键盘与异步状态、字体失败检查，以及本地验证和外部业务结果的证据边界。
