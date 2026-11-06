# Document Writing Skill

面向 Codex / Agent Skills 的中文技术文档写作技能。

核心能力：从需求与项目资料出发，核实事实、设计结构、撰写正文并检查交付质量。适合软件架构设计、技术方案、README、API/协议说明、ADR/RFC、部署排障手册和测试方案。

**与 `natural-writing` 的区别**：本技能侧重文档生产工作流、工程契约和可维护性；自然写作技能侧重语言润色。两者可独立使用。

## 目录结构

```text
skills/document-writing/
├── SKILL.md
└── references/
    ├── document-types.md
    ├── templates.md
    └── review-checklist.md
```

## 安装

### Codex 技能安装器

```text
使用 $skill-installer 从 myzxcvn/document-writing-skill 仓库安装 skills/document-writing
```

### 手动安装（Linux / macOS）

```bash
git clone https://github.com/myzxcvn/document-writing-skill.git
cd document-writing-skill
mkdir -p "$HOME/.agents/skills"
ln -s "$PWD/skills/document-writing" "$HOME/.agents/skills/document-writing"
```

运行前检查目标技能路径不存在，避免覆盖本机已有同名技能。

## 使用

```text
使用 $document-writing 基于当前项目实际代码编写 docs/architecture.md。
解释模块职责、数据流、线程模型、接口契约及异常处理。
未实现的部分明确标记为建议方案。
```

```text
使用 $document-writing 完善 README，核对构建命令、示例和相对链接。
```

```text
使用 $document-writing 评审 API 文档，只列出错误、遗漏及改进建议，不修改文件。
```

## 验证

修改技能后，可使用 Codex 安装环境提供的结构校验器（如果存在）：

```bash
python3 "${CODEX_HOME:-$HOME/.codex}/skills/.system/skill-creator/scripts/quick_validate.py" skills/document-writing
```

该校验器并非本仓库依赖。它检查技能结构，不代表真实项目写作效果得到验证。

## 许可证

MIT，详见 [LICENSE](LICENSE)。
