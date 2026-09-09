# 选题标题新版契约

```yaml
identity:
  technical_id: zuiqiang-shifu-topic-title-lab
  display_name: 最强师傅·选题标题新版
job:
  user: 已有内容方向或内部选题、需要对外标题的短视频创作者
  repeated_task: 把内容方向包装成能吸引目标观众点击、但不提前说完正文的标题
  success: 标题让目标观众产生停留和点击理由，正文能兑现承诺，且标题不是内容摘要
scope:
  owns:
    - 区分选题内核、对外标题和内容承诺
    - 钩子标题、故事标题与搜索标题的模式判断
    - 只看标题或标题加内容方向的输出边界
    - 摘要删除与承诺兑现检查
  excludes:
    - 从零寻找账号方向和内容选题
    - 研究、完整口播、脚本、拍摄和发布
    - 与正文无关的标题党
    - 安装、覆盖或发布全局最强师傅
routing:
  should_trigger:
    - 只给标题、先不要内容或别把答案写进标题
    - 已有内容方向/核心问题/内部短名单时的只看选题
    - 把已有内容方向包装成吸引目标观众的标题
    - 已有内部选题短名单，需要对外可见标题
  should_not_trigger:
    - 完全没有内容方向，要从零找选题
    - 只说“只看选题”但没有方向、问题或可用素材
    - 已有题目，要写研究底稿或完整脚本
    - 只要总结现有内容
    - 想用与正文无关的话题骗点击
  near_neighbors:
    - ../topic-engine: 从零找方向和内部选题，本实验只修其标题输出边界
    - ../viral-factory: 写内容、开头、脚本和发布前标题包装
    - ../opening-selector: 只选开头结构；标题模块不同时接管开头
    - ../expectation-contrast: 已明确真实反差时可作为一个增强器，标题模块仍是唯一 owner
    - ../depth-lab: 为知识口播增加机制、证据和行动深度
inputs:
  required:
    - 内容方向、内部选题或核心问题
    - 目标观众，或足以合理推断目标观众的上下文
  optional:
    - 标题数量
    - 钩子型、故事型或搜索型偏好
    - 用户明确允许使用的事实与案例
outputs:
  artifacts:
    - 对外标题候选
    - 用户明确要求时的独立内容方向栏
  quality_invariants:
    - 标题与正文共享目标观众和核心问题
    - 不提前说完事实原因方法和结论
    - 正文能够兑现标题承诺
    - 不编造不焦虑不使用单一万能公式
    - 标题中的每个具体事实与程度词均能逐项回到用户材料
    - 候选机制和待验证解释只进入正文问题，不提前变成标题答案
workflow:
  decisions:
    - 用户缺的是内容方向还是对外标题
    - 选择钩子故事或搜索模式
    - 选择好奇代入反差利益或搜索驱动
  steps:
    - 冻结内容承诺
    - 建立标题事实白名单
    - 确定停留理由
    - 生成不同驱动候选
    - 删除摘要信息
    - 做逐词事实回查和假设泄漏检查
    - 检查承诺兑现
failure_handling:
  missing_input: 只有用户原话或材料已明确方向时才记为由用户输入完成；否则只问内容方向还是对外标题，不用最小假设替用户定案
  conflict: 用户要求强吸引但不能兑现时，保留真实承诺并降低夸张程度
  out_of_scope: 回到原 topic-engine、viral-factory 或深度实验的相邻流程
trust:
  reads:
    - 用户提供的内容方向、材料和允许使用的事实
  writes:
    - 仅用户批准的实验工作区和证据目录
  external_actions: []
  approval_points:
    - 安装、合并、发布、上传和账号操作另行批准
validation:
  static:
    - package validation
    - quick validation
  routing:
    - 只看标题、从零找方向、写脚本、总结内容和标题党边界
  execution:
    - 女性关系、付费社群、职场效率和故事标题模式
  real_user_signal:
    - 用户在真实选题任务中对新旧标题的明确选择
```
