# moqi-skills

默契（Moqi）的公司级技能包。管理员在 后台 → Skill packs 登记本仓库并固定到某个提交，导入后技能对全体成员可见；移除技能包即归档其中的技能。

每个技能放在自己的目录里（`<技能名>/SKILL.md`）。仓库根目录只放本说明，导入时会忽略它。

## anatomy

把一个技术概念画成真实的机械或仪器：交互式等轴测 SVG 图，可带 WebGL 效果。

- 来源：[wheresryan22/anatomy](https://github.com/wheresryan22/anatomy)，提交 `e9488296a44211c42701ff71705b7901470ec78f`（2026-10-15）。
- 许可：MIT，原作者的版权声明见 `anatomy/LICENSE`。
- 运行要求：沙箱里有 Node.js 20.10 以上和 Chromium（`/usr/bin/chromium`），用于截图和线条检查。

与原版相比的改动：

1. 删除了向公开图库发布作品的部分（`references/publish.md`、`scripts/publish.mjs` 及其辅助脚本 `session.mjs`、`fingerprint.mjs`），并删掉 SKILL.md 中对应的说明。
2. 收窄触发条件：只在用户明确要等轴测图、立体示意图、交互式机械示意图或点名 Anatomy 时使用，普通流程图、图表和幻灯片不用它；默认只做“Figure”规模，“Hero”规模先报估时、等用户同意。
3. SKILL.md 加了 `scope: company` 和一段“In Moqi”说明（路径相对技能目录；示例只带源码，需先构建）。
4. 删除了图片、测试、评测集、CI 配置和示例生成的 HTML 页面（约 10 MB）。示例的构建脚本保留，可随时重新生成。

更新到新版本：从上游取新提交，重复上面的改动，提交到本仓库，再在 后台 → Skill packs 把技能包的 ref 改到新提交并重新导入。
