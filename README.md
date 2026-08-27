# Study Tutor Skill

一个面向研究生学习场景的双语 Study Tutor Skill。它主要为 NTU MSc Data Science 的学习流程设计，也可以用于其他课程。

它不是普通的 PPT 摘要工具，而是帮助你完成：

`课件理解 → 重点提炼 → 课后复习 → 知识串联 → Quiz/Exam 复习 → 练习题 → 双面 Cheatsheet`

## 主要模式

- **Lecture Analysis**：按原课件顺序完整讲解，再重组成清晰的知识体系。
- **Focused Explanation**：针对某一页、公式、图表、算法或代码深入解释。
- **After-Class Review**：生成约 3–5 分钟可读完的课后精简复习。
- **Knowledge Map**：连接同一课程不同 Week 的知识与依赖关系。
- **Quiz / Exam Review**：围绕考试范围、重点、常见考法与易错点复习。
- **Practice**：生成分层练习题，并提供答案与解析。
- **Cheatsheet**：生成一张 A4 纸正反两面的考试工具，并通过资料覆盖、逐题实战、准确性和打印排版验证。

## Cheatsheet 工作流

Cheatsheet 不是普通课程总结，而是一份可以在 Quiz/Exam 中快速查找和直接使用的考试工具。默认输出限制为一张 A4 纸正反两面，并采用以下完整流程：

1. **确认资料范围**
   - 检查所有 Lecture、补充阅读、Tutorial、Assignment、Practice、Past Quiz 和考试说明是否可读，并处理重复版本。
   - 文字、公式、表格、图形、截图和 image-only slides 都纳入覆盖检查。
   - Tutorial 和 Past Quiz 用于判断优先级与验证可用性，但不能代替全部课程内容。

2. **提取考试可用内容**
   - 保留准确的定义、核心概念、适用条件、判断逻辑、算法步骤、重要对比和易错点。
   - 重要公式必须完整呈现，并说明每个符号、使用场景和必要计算步骤。
   - 需要画图时提供考试中能够照着重画的简化图；公式重新排版不清楚时，使用课件中的清晰公式裁图。
   - 专业术语和符号遵循课件原文，以 English terminology 为主，配简短中文提示。

3. **压缩与排版**
   - 输出为可打印的 A4 正反两面，不加入封面、大标题区、背景色或无关装饰。
   - 优先使用紧凑栏目、表格、箭头和对比结构，但不能压缩成难懂的个人简写。
   - 先利用页面空间，再缩小字号；不能一边留下明显空白，一边使用难以阅读的 6–7 pt 小字。

4. **强制实战验证**
   - Coverage audit：逐项核对全部指定资料是否覆盖。
   - Question-by-question audit：逐题检查 Tutorial、Practice 和 Past Quiz/Quiz Example 是否能依靠 cheatsheet 完成。
   - Generality audit：补充可迁移到同类新题的方法，而不是只抄某道例题答案。
   - Accuracy audit：复核术语、公式、正负号、条件、符号、单位、答案和图表。
   - Print audit：确认最终文件恰好两面，没有裁切、重叠，并且正常打印尺寸下清晰可读。

任何一项验证失败，都必须修改并重新检查；只有全部通过后，才能称为可投入使用的 cheatsheet。
## 设计特点

- 中文讲解为主，保留 English terminology。
- 同时理解文字、公式、图表、模型结构和截图标注。
- 课程资料优先；课外补充会明确标记。
- 不确定时不会猜测或假装知道。
- 对公式、算法和代码采用自适应讲解深度。
- Tutorial、Assignment、Past Quiz 会与 Lecture 建立对应关系。

## 安装

### Codex

把本仓库作为 Skill 安装，或将包含 `SKILL.md` 的目录复制/链接到你的 Codex Skills 目录。安装方式可能随 Codex 版本变化，请以当前产品中的 Skills 安装入口或官方说明为准。

### ChatGPT

如果你的 ChatGPT 工作区支持 Personal Skills，可在 Skills 的创建/上传入口导入本仓库目录或打包文件。Personal Skills 的可用性取决于账号和工作区方案。

## 使用示例

上传课件、PDF 或截图后，直接使用自然语言即可：

```text
帮我完整讲解这个课件。
这一页的公式是什么意思？给一个简单数字例子。
生成一个 3–5 分钟课后复习。
我要准备 Week 1–5 的 quiz，帮我系统复习并出题。
根据 lecture、tutorial 和 past quiz 做一张双面 cheatsheet，并逐题验证它是否真的能用。
```

Skill 会自动判断合适的模式，不需要记忆固定命令。

## 仓库结构

```text
study-tutor-skill/
├── README.md
└── SKILL.md
```

## 维护方式

核心行为全部写在 `SKILL.md` 中。常见修改包括：

- 调整讲解详细程度或语言风格。
- 修改课后复习的长度和栏目。
- 调整考试重点判断规则。
- 修改练习题类型、难度和答案格式。
- 更新 Cheatsheet 的资料覆盖、公式呈现、压缩取舍和实战验证规则。

建议每次修改后使用一份真实课程资料测试以下场景：完整课件讲解、截图追问、课后复习、考试复习、练习题和 Cheatsheet。根据实际输出小步迭代，并用 Git commit 记录版本变化。

## 说明

该 Skill 会尽量以课程材料为准，但不能替代老师公布的正式 assessment scope、课程政策或学术判断。对于无法从材料确认的信息，它会明确说明不确定性。
