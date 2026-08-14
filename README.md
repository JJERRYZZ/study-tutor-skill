# NTU Study Tutor Skill

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
- **Cheatsheet**：严格按一张纸正反两面进行高密度信息压缩。

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
根据 lecture、tutorial 和 past quiz 做一张双面 cheatsheet。
```

Skill 会自动判断合适的模式，不需要记忆固定命令。

## 仓库结构

```text
ntu-study-tutor-skill/
├── README.md
└── SKILL.md
```

## 维护方式

核心行为全部写在 `SKILL.md` 中。常见修改包括：

- 调整讲解详细程度或语言风格。
- 修改课后复习的长度和栏目。
- 调整考试重点判断规则。
- 修改练习题类型、难度和答案格式。
- 收紧 Cheatsheet 的压缩与取舍规则。

建议每次修改后使用一份真实课程资料测试以下场景：完整课件讲解、截图追问、课后复习、考试复习、练习题和 Cheatsheet。根据实际输出小步迭代，并用 Git commit 记录版本变化。

## 说明

该 Skill 会尽量以课程材料为准，但不能替代老师公布的正式 assessment scope、课程政策或学术判断。对于无法从材料确认的信息，它会明确说明不确定性。
