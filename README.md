# Study Tutor v2

面向技术课程的研究生学习辅导 Skill。中文讲解为主，保留原始英文术语、公式与课程符号。

A study tutor for graduate technical courses. Explanations are primarily in Chinese, preserving original English terminology, formulas, and course notation.

**Skill 名称 / Skill name:** `study-tutor`

课件理解 → 完整讲解 → 课后复习 → 知识串联 → Quiz/Exam 复习 → 练习 → 双面 Cheatsheet。

Lecture understanding → complete explanation → after-class review → knowledge connections → exam preparation → practice → double-sided cheatsheet.

## 主要模式 / Study modes

| 模式 / Mode | 功能（中文） | Function (English) |
|---|---|---|
| Lecture | 按课件顺序完整讲解，记录页码覆盖，解释公式、图表与例子。 | Explain the full deck in order, track page coverage, and interpret formulas, diagrams, and examples. |
| Focused | 优先回答截图标注、问号、公式或代码中的具体问题。 | Answer specific marked regions, question marks, formulas, or code first. |
| Review | 提供约 3–5 分钟的课后复习，区分理解、记忆与易混淆内容。 | Provide a 3–5 minute review covering understanding, recall, and common confusions. |
| Exam | 根据官方范围、教师说明和样题组织复习，明确证据与不确定性。 | Prepare from official scope, instructor statements, and sample questions, distinguishing evidence from uncertainty. |
| Practice | 生成分层练习、批改答案、诊断错误，并兼顾薄弱点和整体覆盖。 | Generate graded practice, mark answers, diagnose mistakes, and balance weak areas with syllabus coverage. |
| Cheatsheet | 压缩为一张纸正反两面，保留公式、符号、条件与解题规则。 | Compress material into one physical sheet, front and back, retaining formulas, symbols, conditions, and solution rules. |
| Knowledge map | 连接实际提供的跨周资料、先修知识、教程和样题。 | Connect supplied weeks, prerequisites, tutorials, and sample questions. |
| Validation | 检查来源、正确性、完整性和教学质量。 | Check grounding, correctness, completeness, and teaching quality. |

## v2 更新 / Changes in v2

- **模块化工作流：** 按任务加载对应模块，避免将完整讲解替换为简短摘要。  
  **Modular workflows:** Load the relevant module and keep complete teaching distinct from short summaries.
- **课件覆盖记录：** 核对总页数，记录已讲与未讲内容；长课件分段并明确剩余页码。  
  **Coverage ledger:** Verify page counts, track completed and remaining content, and state remaining pages when splitting long decks.
- **资料与证据优先：** 区分课件内容、课外补充和未确认推断，不编造教师要求或考试范围。  
  **Evidence first:** Distinguish course material, external explanations, and uncertain inferences; never invent instructor requirements or assessment scope.
- **可携带课程记录：** 使用模板保存学习进度与薄弱点，不假设 Skill 自带跨会话记忆。  
  **Portable tracker:** Record progress and weak areas in a template without assuming built-in cross-chat memory.

## 文件结构 / Repository structure

| 文件或目录 / File or directory | 用途 / Purpose |
|---|---|
| [SKILL.md](SKILL.md) | 名称、描述、路由与共同教学规则 / Metadata, routing, and shared teaching rules |
| [workflows/](workflows/) | 8 个任务与质量检查模块 / Eight task and validation modules |
| [templates/course-tracker.md](templates/course-tracker.md) | 课程进度与薄弱点模板 / Course progress and weak-point template |
| [V1_REFERENCE.md](V1_REFERENCE.md) | v2 安装包附带的旧版参考，不参与运行 / Legacy reference supplied in the v2 package, excluded from runtime |
| [github-v1-backup-20261009.zip](github-v1-backup-20261009.zip) | 更新前仓库的SKILL.md 和 README.md（公开表述已泛化） / Earlier SKILL.md and README.md with generalized public wording |

## 安装 / Installation

将包含 `SKILL.md`、`workflows/` 和 `templates/` 的完整目录安装到当前 Codex 支持的 Skills 目录，或使用产品提供的 Skills 导入入口。不要只复制 `SKILL.md`，否则模块引用会缺失。安装方式与可用入口以当前环境为准。

Install the complete directory containing `SKILL.md`, `workflows/`, and `templates/` into a Skills directory supported by your Codex environment, or use its Skills import interface. Copying only `SKILL.md` leaves module references unresolved. Available installation methods depend on the environment.

安装或更新后，新开会话以加载最新 Skill；如果仍显示旧版，再重启 Codex。

After installation or updates, start a new session to load the latest skill. Restart Codex if the old version still appears.

## 使用示例 / Usage examples

上传相关课件或截图后，直接用自然语言提出任务，无需记忆模式命令。

Upload the relevant materials and ask naturally; no mode commands are required.

| 中文 | English |
|---|---|
| 帮我完整讲解这个 Week 8 PPT。 | Explain this Week 8 slide deck completely. |
| 这一张图的三个问号分别是什么意思？ | Explain each of the three marked question marks in this diagram. |
| 给我做一个 3–5 分钟的课后复习。 | Give me a 3–5 minute after-class review. |
| 根据 sample quiz 给我出题，答案放最后。 | Generate practice based on the sample quiz, with answers at the end. |
| 把 Week 5–8 做成一页双面 cheatsheet。 | Create a one-sheet, double-sided cheatsheet for Weeks 5–8. |

Cheatsheet 用于实际考试时，是否允许携带以教师或官方考试政策为准。

Permission to bring a cheatsheet into an assessment depends on the instructor or official exam policy.

## 检查与测试 / Checks and testing

**2026-10-09 已完成 / Completed on 2026-10-09:**

- 安装包全部 12 个文件的 UTF-8、名称、描述、文件结构与模块引用检查通过。  
  All 12 package files passed UTF-8, metadata, structure, and module-reference checks.
- 基础调用测试将“完整讲解 Week 8 技术课程 课件”识别为完整讲解任务，并加载 `lecture.md` 和 `validation.md`。  
  A basic invocation recognized the Week 8 technical-course full-lecture request and loaded `lecture.md` and `validation.md`.
- GitHub 同步后，文件哈希与准备上传的版本一致；教学流程保持原样；公开名称和课程背景已泛化。  
  After GitHub synchronization, file hashes matched the prepared files; teaching workflows remain unchanged; public naming and course context have been generalized.

**测试边界 / Test limitations:** 基础测试未附实际课件，因此不能据此声称完整课件讲解质量已通过回归测试。真实 课程课件及不同模型上的完整表现仍需实际验证。

No real lecture deck was supplied for the basic test, so it does not establish full lecture-teaching quality. Regression testing with real course materials and different models remains pending.

## 维护与恢复 / Maintenance and recovery

共同规则在 `SKILL.md`，各模式在 `workflows/`；修改后应检查引用并使用真实课程资料验证。Git 提交历史和旧版备份可用于恢复。

Shared rules live in `SKILL.md`; mode-specific rules live in `workflows/`. After changes, check references and validate with real course materials. Git history and the legacy backup support recovery.

## 通用版本 / General version

本仓库采用通用名称 Study Tutor，不绑定特定学校或专业。调整仅涉及名称与课程背景，保留 v2 的教学流程。归档文件同样使用通用表述。

This repository uses the general name Study Tutor and is not tied to a specific university or major. Only naming and course context have been generalized; v2 teaching workflows are preserved. Archived files also use general wording.
