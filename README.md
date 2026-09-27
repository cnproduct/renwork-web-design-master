# RenWork Web Design Master

面向 Agent Skills 工作流的网页设计技能：从真实内容与品牌出发，把视觉判断落实到响应式布局、中英文排版、可访问交互和可复核的验收。

**入口：[SKILL.md](SKILL.md) · 版本：1.0.0 · MIT · 可选工具仅需 Python 3.9+**

## 适用任务

- 新建品牌站、B2B 产品页、落地页和 Web 应用界面。
- 优化字体配对、字阶、中文换行、内容密度和移动端布局。
- 审计或修复现有页面的视觉、键盘交互、对比度与状态反馈。

保留用户的品牌与技术栈；不以“去 AI 味”为由禁止系统字体或强制套用另一种模板。真实业务事实、部署与收录需要各自的验证。

## 安装

Codex（全局安装；目标目录须不存在）：

```bash
git clone https://github.com/cnproduct/renwork-web-design-master.git ~/.codex/skills/renwork-web-design-master
```

Claude Code（项目内安装）：

```bash
git clone https://github.com/cnproduct/renwork-web-design-master.git .claude/skills/renwork-web-design-master
```

Cursor、Antigravity 及其他客户端：将**完整文件夹**放入该客户端当前版本支持的 Skill 发现目录，或显式让代理读取本仓库的 `SKILL.md`。保留相对目录，不能只复制入口而丢失引用。这里只保证标准 Skill 文件结构；未对所有客户端版本完成运行验收。

已有安装先检查本地改动，再使用 `git pull --ff-only` 更新；不要强制覆盖自定义修改。安装后开启新会话或按客户端提供的方式重新加载技能。

## 调用示例

```text
使用 $renwork-web-design-master，优化现有制造商产品详情页。
保留公司名称、品牌色、真实参数和当前技术栈；重点改善移动端参数阅读与询盘入口，完成后报告实际检查结果。
```

```text
使用 $renwork-web-design-master，只审计这个页面的中文换行、字号层级和键盘访问，不修改代码。给出可复现的问题与最小修复建议。
```

```text
使用 $renwork-web-design-master，修复手机端长标题溢出。
追踪共享组件与其他调用点，不通过隐藏溢出裁掉文字，保留现有设计。
```

## 可选辅助工具

在本仓库根目录运行：

```bash
python3 scripts/design_math.py contrast '#334155' '#ffffff'
python3 scripts/design_math.py fluid 16 20 360 1280
python3 scripts/design_math.py self-test
```

`contrast` 普通文字使用 4.5:1 门槛；确认属于大文字后可加 `--large` 使用 3:1。失败退出码 1，输入错误退出码 2。仅支持不透明 `#RGB` / `#RRGGBB`；不抓取网页、不处理透明叠加或图片背景。

`fluid` 四个参数依次为最小字号、最大字号、最小视口、最大视口，单位 CSS px；`--root` 默认 16，是公式假设，不会修改用户根字号。生成后仍需检查缩放与真实字体。

## 文件与验收边界

| 文件 | 用途 |
|---|---|
| [SKILL.md](SKILL.md) | 触发范围、执行流程与交付约束 |
| [design-layout.md](references/design-layout.md) | 按用户任务组织页面、组件和空间 |
| [typography.md](references/typography.md) | 字体选择、流式字号、中文和多语言 |
| [verification.md](references/verification.md) | 浏览器、键盘、对比度与证据要求 |
| [foundations.css](assets/foundations.css) | 按需摘取的 CSS 起点，不是完整主题 |
| [design_math.py](scripts/design_math.py) | 对比度与流式字号核算、自检 |
| [sources.md](references/sources.md) | 上游入口、标准及原稿修订说明 |

CI 只运行数学工具自检，不证明最终页面的可用性、完整无障碍合规或商业效果。每个使用项目都应执行与其改动范围相匹配的浏览器验收。

与 `renwork-industry-site-master` 配合时，沿用其已批准的公开事实与采购目标；两个 Skill 各自可独立使用。
