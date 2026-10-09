# NTU Study Tutor v2

Graduate-level Chinese-first tutor for NTU MSc Data Science and other technical courses.

## What changed from v1
- Separate workflows for full lecture, focused images, after-class review, exam review, practice and cheatsheet.
- Coverage ledger to prevent silent omission of long slide decks.
- Evidence-first explanations and explicit uncertainty labels.
- Formula/diagram/answer validation rules.
- Portable course tracker; no unsupported claims of cross-chat memory.

## Install
Place this directory in a supported Agent Skills directory (with `SKILL.md` at the root of the skill directory), or upload/import via the relevant product's supported Skills UI. Product access and UI vary. `V1_REFERENCE.md` is archival and not part of the runtime workflow.

## Use
Ask naturally: “帮我完整讲解这个 Week 8 PPT”, “这一张图的三个问号分别是什么意思”, “给我做 3–5 分钟课后复习”, “根据 sample quiz 给我出题”, “把 Week 5–8 做成一页双面 cheatsheet”.

## Test status
Structural checks only. Not yet regression-tested against actual NTU Week 8 slides or Sol 6.1 model output.

## Repository sync — 2026-10-09

- Runtime files match the provided `ntu-study-tutor-v2.zip`; teaching logic is unchanged.
- Skill name: `ntu-study-tutor`. Keep `SKILL.md`, `workflows/`, and `templates/` together when installing.
- Checks passed: UTF-8 files, YAML name/description, module references, and a basic SD6124 Week 8 lecture-task routing test loading `lecture.md` and `validation.md`.
- No real lecture deck was supplied for that test; full lecture regression testing remains pending.
- Previous GitHub version: `github-v1-backup-20261009.zip` (original SKILL.md and README.md). `V1_REFERENCE.md` is the archive supplied in the v2 package.
- Workflows: `lecture`, `focused`, `review`, `exam`, `practice`, `cheatsheet`, `knowledge-map`, and `validation`; portable tracker: `templates/course-tracker.md`.
