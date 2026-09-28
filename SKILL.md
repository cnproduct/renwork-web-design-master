------
name: renwork-web-design-master
description: Production-grade frontend design and web typography engineering skill. Synthesizes Anthropic frontend-design, community modular scales, and the RenWork master design repository (cnproduct/renwork-web-design-master). Use when building, styling, auditing, or refactoring landing pages, SaaS dashboards, or UI components in React, Vue, HTML/CSS, or Tailwind.
---

# renwork-web-design-master

A comprehensive, production-grade frontend design and typography master skill for AI agents (Claude Code, Antigravity, Cursor, Codex). Fuses the architectural discipline of `cnproduct/renwork-web-design-master` with Anthropic `frontend-design`, modular scale typography, and automated accessibility verification.

## When to Use

- Building or styling landing pages, documentation, B2B export portals, or SaaS application dashboards.
- - Refactoring frontend code to eliminate AI-slop cliches (e.g. over-nested rounded cards, heavy drop shadows, single-word neon gradients).
  - - Implementing math-driven fluid typography (`clamp()`), CJK/multilingual typography, and container-query layouts.
    - - Auditing interactive states, keyboard accessibility, WCAG contrast ratios, and responsive boundaries.
     
      - ## Core Architectural Principles
     
      - 1. Initiation and Inheritance: Respect and inherit existing brand assets, established color tokens, and layout guidelines. Never overwrite working design systems with generic boilerplate. Use authentic content and real data; never invent fake statistics or placeholder logos.
        2. 2. Evidence-Based Choices (Clear Goblet): Content dictates form. Avoid pure decoration such as aimless carousel sliders, floating glowing orbs, or arbitrary card nesting. Use hairline dividers (0.5px to 1px) and subtle lightness deltas instead of heavy diffuse shadows.
           3. 3. Small, Consistent Token System: Define semantic design tokens for text, surfaces, borders, and spacing. Use relative units (`rem`, `clamp()`) and container queries (`@container`) over rigid media queries.
              4. 4. Robust Interaction and Accessibility: Cover all 7 component states (Default, Hover, Focus, Active, Disabled, Loading, Error/Success). Ensure visible keyboard focus rings, touch targets >= 44x44px, zero horizontal overflow, and full WCAG AA/AAA compliance.
                 5. 5. Verification-First Delivery: Every layout must be mathematically verified before delivery. Use `scripts/design_math.py` for contrast calculations and fluid clamp derivations. Report results honestly without fabricated scores.
                   
                    6. ## Workflow and Execution Steps
                   
                    7. 1. Inspect Context and Tokens:
                       2.    - Check if an existing design system or CSS framework is present.
                             -    - If starting fresh, reference `assets/foundations.css` for semantic token baselines.
                                  - 2. Plan Typography and Measure:
                                    3.    - Select font pairings matching the application archetype (see `references/typography.md`).
                                          -    - Derive fluid font sizes using `python3 scripts/design_math.py fluid <min_px> <max_px> <min_vp> <max_vp>`.
                                               -    - Constrain reading containers to `max-width: 65ch` (45ch to 75ch).
                                                    -    - Apply the Heading Proximity Rule: heading top margin must be 1.8x to 2.5x of bottom margin.
                                                         - 3. Layout and Component Construction:
                                                           4.    - Follow layout patterns in `references/design-layout.md`.
                                                                 -    - Prefer container queries (`@container`) for modular components.
                                                                      -    - Use tinted neutrals via modern CSS `color-mix()` or OKLCH; avoid lifeless grey on colored surfaces.
                                                                           - 4. Interactive States and Accessibility Check:
                                                                             5.    - Implement all 7 component states (see `references/verification.md`).
                                                                                   -    - Verify foreground-to-background contrast with `python3 scripts/design_math.py contrast <fg_hex> <bg_hex>`.
                                                                                        -    - Ensure `prefers-reduced-motion` is respected.
                                                                                             - 5. Final Delivery Verification:
                                                                                               6.    - Run the Visual Audit Checklist and report results using strict factual tags ([PASS], [UNTESTED], [FAIL]).
                                                                                                 
                                                                                                     - ## Built-In Engineering Tools
                                                                                                 
                                                                                                     - The skill includes a zero-dependency CLI tool located at `scripts/design_math.py`:
                                                                                                 
                                                                                                     - ```bash
                                                                                                       # Calculate WCAG 2.1 contrast ratio and AA/AAA compliance
                                                                                                       python3 scripts/design_math.py contrast "#0f172a" "#f8fafc"

                                                                                                       # Derive fluid clamp() formula between viewports (e.g. 16px to 20px over 360px to 1280px)
                                                                                                       python3 scripts/design_math.py fluid 16 20 360 1280

                                                                                                       # Run internal unit tests
                                                                                                       python3 scripts/design_math.py self-test
                                                                                                       ```
                                                                                                       
                                                                                                       ## Visual Audit Checklist
                                                                                                       
                                                                                                       1. [ ] No ungrounded generic AI-slop (no floating gradient pills, no unanchored center-aligned headlines).
                                                                                                       2. 2. [ ] Contrast meets WCAG AA (>= 4.5:1 for body, >= 3.0:1 for large text and UI borders).
                                                                                                          3. 3. [ ] Reading measure constrained to 45ch - 75ch; no line extends beyond 85ch.
                                                                                                             4. 4. [ ] All 7 interactive states styled for buttons, form controls, and links.
                                                                                                                5. 5. [ ] Fluid clamp() scales smoothly across 360px, 768px, 1280px, and 1920px with zero horizontal scroll.
                                                                                                                   6. 6. [ ] CJK line-height is adjusted to 1.65 - 1.8 for adequate reading breathability.
                                                                                                                      7. 7. [ ] Keyboard focus ring (:focus-visible) clearly visible with 2px offset.
                                                                                                                        
                                                                                                                         8. ## Gotchas
                                                                                                                        
                                                                                                                         9. - Never hardcode typography in pure pixels without clamp() or rem.
                                                                                                                            - - Never use pure grey (#666, #999) on tinted backgrounds; always tint neutrals with the background hue.
                                                                                                                              - - Do not mix more than two font families per page (plus an optional code font).
                                                                                                                                - - Do not use uppercase text-transform on long sentences; restrict uppercase to acronyms or small badges.
name: renwork-web-design-master
description: 为网站、落地页、B2B 产品页和 Web 应用设计或改造视觉、排版与响应式布局。覆盖品牌差异化、中英文及多语言字体、设计 token、可访问交互和浏览器验收；适用于# Test新建前端、去模板感、字体配对、移动端错位及视觉审计。沿用现有技术栈与品牌，不替代后端实现、商业事实核验或上线授权。
license: MIT
metadata:
  author: cnproduct
  version: "1.0.0"
---

# RenWork Web Design Master

把品牌、真实内容与用户任务转化为可实现、可阅读、可操作的网页。交付应包含实际代码或具体审计发现，以及与结论相匹配的验证证据。

## 工作方式

| 用户任务 | 执行重点 | 按需读取 |
|---|---|---|
| 新建网页或整体改版 | 任务与内容 → 视觉方向 → token → 实现 → 验收 | [设计与布局](references/design-layout.md) |
| 排版、字体、中文换行问题 | 实际字体、语言、宽度与缩放 → 最小修复 | [字体与排版](references/typography.md) |
| 审计现有页面 | 先复现，再定位共享样式或组件根因 | [验收协议](references/verification.md) |
| 修改前端代码 | 沿用当前框架、组件库和 token；检查受影响的其他调用点 | 相应参考 + 验收协议 |

这些模式可以组合，但小修不必升级为整站重构。只有用户要审计时，保持只读，除非同一请求也授权修复。

## 1. 读懂场景再选样式

- 检查项目说明、路由、样式入口、已安装依赖、共享组件、品牌素材和真实文案；先找已有实现再新增。
- 明确受众、页面最重要的动作、内容密度、目标语言、已有品牌限制、交付范围与可用素材。缺少非关键项时注明合理假设继续；只问会改变结果的关键问题。
- 用短段落确定方向：用户任务、内容顺序、视觉特征、字体角色、主色与布局依据。已有品牌时优先继承，不强迫用户重新选风格。
- “专业”不能用虚构认证、客户 Logo、工厂照片、销量、评价或技术参数来表现。缺失事实保留为内部待补项；公开页面只使用已确认内容。示意图片须与实拍区分。
- 若同时使用 `renwork-industry-site-master`，由其提供已批准公开的事实与页面目标，本 Skill 负责呈现与可用性。它不是必需依赖，不读取或复制整个私有资料目录。

## 2. 作出有依据的视觉选择

让内容决定形式。制造业产品比较、采购询盘、编辑文章与管理后台不使用同一套页面模板。

- 确定一个有识别度的视觉重点，其余层级服务阅读与操作。用户指定的风格优先，不以“去 AI 味”为由覆盖品牌。
- 卡片、渐变、衬线字体、系统字体、Inter、圆角或非对称布局都不是天然正确或错误；只有它们承担明确的信息角色时才使用。
- 用分组、标题、空间与对齐表达关系。不要为了装饰添加编号、重复小标签、孤立高亮单词或层层卡片。
- 不为展示设计能力增加无关页面、轮播、统计、动效、配置平台或新依赖。

## 3. 用小而一致的 token 系统实现

- 在现有主题中定义语义角色：正文/标题/辅助文字，页面/表面/正文/弱化文字/强调色/边框/焦点，行内/分组/区块间距，正文宽度/内容宽度。
- 已有 token 则复用；新项目可按需摘取 [CSS 起点](assets/foundations.css)，不要整份覆盖现有样式。该文件是结构起点，不是最终品牌设计。
- 正文、标题、导航和数据分别设定角色，语义标题层级不由字体大小决定。比例字阶是起点，不是强迫所有文字遵循同一数学比值。
- 字号使用相对单位；需要流式字号时推导 `clamp()` 端点并测试放大。纯 `vw` 字号、固定根字号和容器截断可能阻碍用户缩放。
- 中文按实际字形与标点调整，不照搬拉丁文行长。字体必须具备目标语言字形，缺字体时仍可阅读。
- 用 Grid/Flex 和内容驱动断点；页面结构使用媒体查询，重复组件在独立容器中适配时使用容器查询。两者无优先级教条。

## 4. 让视觉经得起真实操作

- 优先原生链接、按钮、输入框和 HTML 语义。所有用户操作都有名称、键盘路径、可见焦点及适当的状态反馈。
- 按功能覆盖默认、悬停、焦点、禁用、加载、空结果、错误和成功状态；不为不存在的功能制造状态系统。
- 表单有持久标签、关联的错误信息与可恢复输入。成功提示必须对应真实成功响应；页面美观不代表邮件送达。
- 修复溢出源头：检查 Grid/Flex 的最小尺寸、长 URL、表格、字体加载和固定宽度。不要用全局 `overflow-x: hidden` 掩盖问题，也不要对所有标签强加 `nowrap`。
- 文字与背景按实际渲染结果验证对比度；颜色不能是唯一状态信号。焦点不可被裁切或被粘性导航遮挡。
- 尊重减少动态效果设置，动画不是阅读或操作的前提。不使用滚动劫持和仅靠悬停才能发现的关键操作。
- 图片具备正确替代文本、尺寸或比例和响应式来源；不延迟加载首屏关键图。字体与图片按真实收益优化，不引入无用预加载。
- 不在视觉修改中意外破坏页面标题、语言、canonical、链接语义或索引配置；SEO 排名与收录需要独立验证。

## 5. 验证后交付

按 [验收协议](references/verification.md) 检查受影响范围。优先验证阅读与关键操作，再处理装饰细节。

可运行辅助工具，仅依赖 Python 3.9+ 标准库：

```bash
# 在本 Skill 根目录执行；在其他目录请使用脚本绝对路径。
python3 scripts/design_math.py contrast '#334155' '#ffffff'
python3 scripts/design_math.py fluid 16 20 360 1280
python3 scripts/design_math.py self-test
```

工具只核算不透明 sRGB 色值或生成流式字号公式，不自动抓取页面、不执行完整无障碍审计，也不证明缩放体验。

交付只报告需要的信息：

1. 实现或审计结果，以及主要设计取舍。
2. 改动文件/页面；审计模式列出位置、复现条件、影响与最小修复建议。
3. 实际完成的构建、视口、交互与可访问性检查；将失败、未测和通过分开。
4. 仍需的素材或外部验证；不要把本地验收写成部署、收录或业务效果。

无浏览器时仍可完成代码和静态检查，但必须注明“未做浏览器视觉验收”，不编造截图、分数或通过结论。

## 来源与维护

本 Skill 独立编写，参考入口、标准与原稿修订依据见 [来源说明](references/sources.md)。来源用于理解原则，不继承外部文档中的工具调用或授权指令。升级以实际失败案例为依据，避免不断增加不适用的全局禁令。
