# Power Electronics Paper Distill

一个面向 Codex 的电力电子论文蒸馏 Skill。它把逆变器、变换器、调制、建模、控制、稳定性、损耗、热设计、仿真、HIL 和样机论文转换为：

1. 有页码证据的中文精读笔记；
2. 可审计、可复用的科研方法卡。

它适合把阅读结果沉淀为后续研究可调用的知识，而不是只生成摘要。

## 安装

将本仓库目录复制或链接到 Codex 的 skills 目录，目录名保持为 `power-electronics-paper-distill`。随后在任务中输入：

```text
使用 $power-electronics-paper-distill 蒸馏这篇论文。
```

也可以直接提供 PDF 路径并要求产出中文精读笔记与方法卡。

## 输出

```text
paper-distill/<paper-id>/
|-- reading-note.md
|-- evidence-ledger.md
`-- method-cards/
    `-- <method-name>.md
```

Skill 强制区分原文结论、复核推导和迁移假设，并检查符号、单位、坐标、因果性、实现约束、稳定性范围与证据等级。

## 仓库范围

本仓库只包含 Skill 指令、模板和审计清单。它不包含论文 PDF、论文截图、仿真模型、实验数据或未发表研究材料。使用者应自行遵守论文版权和数据保密要求。

## License

MIT. See [LICENSE](LICENSE).
