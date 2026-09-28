# First Principles Thinking for Codex

A compact Codex skill for testing important decisions against verified facts, hard constraints, assumptions, and material unknowns.

## Installation

### Copy

```bash
git clone https://github.com/tt-a1i/first-principles-skill.git
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R first-principles-skill "${CODEX_HOME:-$HOME/.codex}/skills/"
```

### Symlink

```bash
mkdir -p "$HOME/skills"
git clone https://github.com/tt-a1i/first-principles-skill.git "$HOME/skills/first-principles-skill"
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
ln -s "$HOME/skills/first-principles-skill" "${CODEX_HOME:-$HOME/.codex}/skills/first-principles-skill"
```

## Usage

Invoke it explicitly:

```text
使用 $first-principles-skill 分析我们是否应该拆分微服务。
```

Codex can also select it automatically for requests such as:

- “用第一性原理分析这个方案。”
- “这个架构的关键假设是什么？”
- “不要照搬行业惯例，从事实和约束重新推导。”
- “Is this proposal supported by evidence, or are we just following convention?”

Ordinary architecture explanations and routine design reviews do not trigger the skill merely because they concern architecture or design.

## Behavior

The skill:

- separates verified facts, constraints, assumptions, and unknowns;
- attributes unverified user-provided data and accepts explicit hypothetical premises, keeping conclusions conditional on them;
- identifies key variables, causal relationships, or cost components and distinguishes objective limits from current implementation choices;
- treats conventional solutions as candidates rather than automatic winners or losers;
- prefers lower complexity among solutions that meet the success criteria, accounting for reliability, maintenance, and long-term effects;
- answers concisely by default and expands when requested or when uncertainty or risk warrants it;
- follows the requested format without forcing a recommendation when the user only wants assumptions or a comparison.

## Structure

```text
first-principles-skill/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── README.md
└── LICENSE
```

## License

MIT License. See [LICENSE](LICENSE).
