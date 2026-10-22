# 最强师傅 V3.0｜模块索引

根入口是 [SKILL.md](SKILL.md)，全包只有它一个 `SKILL.md`；下面列的模块文件都叫 `MODULE.md`，由根入口按需调用，不单独安装。怎么装见 [INSTALL.md](INSTALL.md)。AI 还必须读取 [不可跳步执行协议](WORKFLOW_PROTOCOL.md) 和 [去 AI 味表达规则](VOICE_RULES.md)，再根据用户真正要的成品，只读取一个主模块；确有窄缺口时，最多再读取一个增强模块。

## 主模块

- [topic-engine](topic-engine/MODULE.md)：从零找内容方向、筛选选题；默认离线，出 3–5 个候选、推荐一个
- [account-launch](account-launch/MODULE.md)：账号定位、赛道、冷启动
- [viral-factory](viral-factory/MODULE.md)：完整口播、结构重写、爆款表达
- [ip-story](ip-story/MODULE.md)：个人 IP、创始人故事、品牌故事
- [growth-engine](growth-engine/MODULE.md)：涨粉问题与内容增长
- [monetization](monetization/MODULE.md)：商业化、报价与变现节奏
- [director-training](director-training/MODULE.md)：编导能力训练
- [pitfall-guide](pitfall-guide/MODULE.md)：自媒体常见误区与纠偏

## 新版窄模块

- [topic-title-lab](topic-title-lab/MODULE.md)：已有方向之后，只做对外标题
- [depth-lab](depth-lab/MODULE.md)：知识稿的机制、证据、影响与深度成稿
- [opening-selector](opening-selector/MODULE.md)：从材料中选择一个合适的开头
- [expectation-contrast](expectation-contrast/MODULE.md)：材料支持时增强真实反差
- [conflict-stakes](conflict-stakes/MODULE.md)：补足故事目标、阻力、利害和选择
- [motivation-delivery](motivation-delivery/MODULE.md)：检查前端承诺能否被后端交付接住

## 马师傅模块

- [copy-craft](ma-shifu/copy-craft/MODULE.md)：文案手艺，成稿后改句子（太空、说教、像广告、要不要加对话、太书面想更像真人说），也给开头/标题补试用候选
- [pain-point-converter](ma-shifu/pain-point-converter/MODULE.md)：卖货备选，产品痛点与销售表达
- [itch-marketing-engine](ma-shifu/itch-marketing-engine/MODULE.md)：卖货备选，痒点、预拥有感和身份表达

卖货备选只在用户明确带货或获客时进；做内容时留在编导模块，句子交给 copy-craft。

## 示范稿

- [examples/](examples/)：一篇方法类口播、一篇深度稿，带完整的步骤记录、改句子和真人润色前后对照；一份南北差异的选题示范（默认离线，对外格式照它写）

## 读取边界

- 不要一次把所有模块串成流水线。
- 每个模块自己的步骤都必须按顺序完成；用户已有输入算该步已完成，只有用户明确要求才可跳过。
- 深度口播由 `depth-lab` 负责深度；只有用户选择融合爆款风格时，才内置 `viral-factory` 的表达层，这不算第二个主模块。
- 任何模块提到的平台比例、分发周期、算法或产品规则，都要先看当前官方信息；核实不了，写成带时间的观察，不在成稿里加免责句。
- 成稿顺序：编导模块定结构和判断 → 按需用 copy-craft 改句子 → 过 [VOICE_RULES.md](VOICE_RULES.md) 终检（含广告味）→ 口播类按 VOICE_RULES 第七节做真人润色（极端情绪词、生活化、口语化、热梗）→ 出声读。改句子和真人润色不算增强模块。
- 结尾不负责给方法：方法类的方法放在正文讲透，结尾不布置作业；机制解释类深度稿默认不带行动段。
- 版本变更见 [CHANGELOG.md](CHANGELOG.md)。
- 内部术语不直接倾倒给普通用户，最终输出应是选题、标题、口播、判断或行动建议。
