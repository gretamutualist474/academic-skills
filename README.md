# Academic Skills

**GitHub:** [LigphiDonk/academic-skills](https://github.com/LigphiDonk/academic-skills)

`academic-skills` 是一组面向 AI Agent 的本地技能仓库。每个 skill 都是一套可复用的任务流程，Agent 识别到对应场景后，可以直接按 `SKILL.md` 执行，减少重复提示和人工整理成本。

## 仓库内容

目前仓库包含 1 个 skill：

- `real-literature-trace/` - `Real Literature Trace`

这个 skill 适合做下面这些任务：

- 搜索真实可追溯的学术文献
- 整理文献综述和核心文献表
- 核验 DOI、出版社页、CNKI 链接等来源
- 筛选近五年的高质量论文
- 组织中英文混合文献

## Skill 是什么

你可以把 skill 理解成给 AI Agent 的“任务手册”。

- 把一类重复任务封装成固定流程
- 让 Agent 在特定任务上更稳定、更可控
- 方便通过 GitHub 仓库安装、更新和分发

## 安装方式

如果你的环境支持 `npx skills`，可以直接从这个仓库安装。

安装整个仓库：

```bash
npx skills add LigphiDonk/academic-skills
```

只安装这个 skill：

```bash
npx skills add LigphiDonk/academic-skills --skill "Real Literature Trace"
```

如果你的 `skills` 版本按技能 `id` 匹配，可以尝试：

```bash
npx skills add LigphiDonk/academic-skills --skill real-literature-trace
```

如果仍然提示找不到 skill，可以先不带 `--skill`，因为当前仓库只有 1 个 skill：

```bash
npx skills add LigphiDonk/academic-skills
```

## 使用示例

安装后，可以直接让 Agent 按这个 skill 的方式工作，例如：

- `帮我找近五年的真实文献`
- `整理一个关于 XXX 的核心文献表`
- `把这些论文按 CNKI / DOI / 期刊来源分类`

## 说明

- `SKILL.md` 里定义了这个 skill 的触发场景、工作流和输出要求
- 安装完成后，重启 Codex 或重新加载 Agent 环境，让新 skill 生效
- 如果你只是想本地查看内容，直接打开 [`real-literature-trace/SKILL.md`](./real-literature-trace/SKILL.md) 即可
