# AAAI-Review-Simulator

> Unofficial AAAI-style multi-reviewer prompt for strict paper self-assessment, meta-review simulation, and revision planning.

[中文说明](#中文说明) | [English](#english)

## 中文说明

**AAAI-Review-Simulator** 是一个非官方的 AAAI-style 论文模拟审稿 Prompt。它适合在投稿前对 AI / CS 论文做严格自查：让模型模拟多位 reviewer 和 SPC/AC meta-reviewer，指出技术、实验、创新性、写作结构和合规风险。

它不是 AAAI 官方工具，也不能预测真实接收结果。它的用途是帮助作者更早发现问题、安排修改优先级，并减少“看起来完整但实际达不到顶会标准”的风险。

### 主要功能

- 模拟 4 类 reviewer：
  - Technical Soundness
  - Experiments & Reproducibility
  - Novelty, Significance & Related Work
  - Writing, Structure & Compliance
- 模拟 SPC/AC-style meta-review。
- 明确区分 Fatal / Major / Minor issues。
- 给出 AAAI-style rating 和 confidence。
- 检查 title / abstract / main paper consistency。
- 检查 baseline、ablation、random seed、hyperparameters、hardware、statistics、failure cases。
- 输出 priority revision plan 和 one-week emergency revision plan。
- 强制 evidence-grounded criticism，减少模型脑补。

### 文件说明

```text
prompts/aaai_review_full_zh.md       # 中文完整版，推荐用于正式自查
prompts/aaai_review_compact_zh.md    # 中文精简版，适合快速评审
prompts/aaai_review_full_en.md       # 英文完整版，适合英文论文作者使用
docs/usage_zh.md                     # 中文使用说明
docs/ethics.md                       # 使用边界与伦理说明
docs/limitations.md                  # 局限性说明
examples/example_input.md            # 输入示例
```

### 快速使用

1. 打开 `prompts/aaai_review_full_zh.md`。
2. 把论文 PDF、LaTeX、摘要、实验表格或补充材料提供给模型。
3. 粘贴 prompt。
4. 要求模型严格按照输出结构生成模拟审稿报告。
5. 根据 P0 / P1 / P2 修改计划优先修论文。

### 推荐模型设置

- 使用支持长上下文的模型。
- 尽量上传完整论文，而不是只给摘要。
- 如果评估 related work，请开启网络搜索或提供参考文献列表。
- 如果没有网络搜索，请不要要求模型列出具体漏引论文标题。

### 重要免责声明

This project is unofficial and is not affiliated with AAAI.

本项目不是 AAAI 官方审稿系统，不代表 AAAI 官方政策、官方评分表或真实录用概率。输出结果只能用于作者自查、修改规划和研究训练，不能用于操纵、攻击、绕过或干扰任何真实同行评审系统。

## English

**AAAI-Review-Simulator** is an unofficial AAAI-style prompt for strict paper self-assessment. It simulates multiple reviewers and an SPC/AC-style meta-reviewer to identify weaknesses before submission.

### Features

- 4 simulated reviewer roles: technical soundness, experiments/reproducibility, novelty/related work, and writing/compliance.
- SPC/AC-style meta-review.
- Fatal / Major / Minor issue separation.
- AAAI-style rating and confidence calibration.
- Evidence-grounded criticism.
- Priority revision plan and 7-day emergency revision plan.

### Disclaimer

This project is unofficial and is not affiliated with AAAI. It does not predict actual acceptance decisions and should not be used to manipulate or interfere with real peer-review systems.

## License

MIT License. See [LICENSE](LICENSE).
