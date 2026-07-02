# 使用说明（中文）

## 适用场景

这个 prompt 适合以下情况：

- AAAI / IJCAI / NeurIPS / ICLR / ACL / EMNLP / ICRA / IROS 等 AI / CS 论文投稿前自查。
- 论文已经有完整摘要、方法、实验和结论。
- 作者想知道当前版本更像 4 分、5 分、6 分还是 7 分论文。
- 作者需要一周内优先修改计划。

## 推荐流程

1. 上传论文 PDF 或 LaTeX 源码。
2. 上传补充材料、实验表格、appendix 或 rebuttal 草稿。
3. 粘贴 `prompts/aaai_review_full_zh.md`。
4. 要求模型：

```text
请严格按照这个 prompt 评审我上传的论文，不要给虚高分。
```

5. 得到报告后，优先处理：
   - P0 fatal issues
   - Reviewer 2 missing experiments
   - Reviewer 3 novelty / related work gaps
   - Title / abstract / main paper mismatch

## 快速模式

如果只想快速判断能不能投，使用：

```text
prompts/aaai_review_compact_zh.md
```

## Related Work 检查建议

如果模型不能联网或你没有提供完整参考文献，prompt 会要求它不要编造具体论文标题。  
如果你希望它真正检查漏引，请同时提供：

- 当前 reference list；
- 你认为最接近的 5–10 篇论文；
- 或开启网络搜索。

## 如何解释分数

- 7+：有 reviewer 明确支持接收，但仍可能被其他 reviewer 拉低。
- 6：有竞争力但缺陷明显，取决于其他 reviewer 是否认可贡献。
- 5：略低于接收线，通常需要补强实验、创新性定位或写作结构。
- 4：论文完整但达不到 AAAI Main Track 标准。
- 3 或以下：存在结构性硬伤。

## 常见误用

不要把输出当成真实录用概率。  
不要根据一次模型评审就决定投稿或放弃。  
不要让模型编造“某 reviewer 会怎么想”。  
不要用它替代真实导师、合作者或领域专家的判断。
