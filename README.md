# ai-harnesses

Personal Skills, Agents and other AI resources for Agentic workflows by [Francois Gerthoffert](https://github.com/Fgerthoffert).

This repository is also a **GitHub Copilot CLI plugin marketplace**, making it easy to install the plugins it contains directly from the CLI.

---

## Plugins

### `fgerthoffert-personal`

A personal plugin containing placeholder skills for:

| Skill | Description |
|---|---|
| [`writing-style`](./plugins/fgerthoffert-personal/skills/writing-style/SKILL.md) | Applies Francois Gerthoffert's personal writing style when generating or editing text. |
| [`documentation`](./plugins/fgerthoffert-personal/skills/documentation/SKILL.md) | Generates documentation following Francois Gerthoffert's preferred structure and style when working in an Agentic context. |

> **Note:** Both skills are currently placeholders. Detailed guidelines and examples will be added over time.

---

## Installation

### Install via marketplace

Register this repository as a Copilot CLI marketplace:

```sh
copilot plugin marketplace add Fgerthoffert/ai-harnesses
```

Then install the personal plugin:

```sh
copilot plugin install fgerthoffert-personal@ai-harnesses
```

### Install directly

You can also install the plugin directly without registering the marketplace:

```sh
copilot plugin install Fgerthoffert/ai-harnesses:plugins/fgerthoffert-personal
```

### Verify the installation

```sh
copilot plugin list
```

Or inside an interactive Copilot session:

```
/skills list
```

---

## Repository structure

```
.github/
└── plugin/
    └── marketplace.json          # Marketplace configuration
plugins/
└── fgerthoffert-personal/
    ├── plugin.json               # Plugin manifest
    └── skills/
        ├── writing-style/
        │   └── SKILL.md          # Writing style skill (placeholder)
        └── documentation/
            └── SKILL.md          # Documentation generation skill (placeholder)
```
