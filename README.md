# ai-harnesses

Personal Skills, Agents and other AI resources for Agentic workflows by [Francois Gerthoffert](https://github.com/Fgerthoffert).

This repository is also a **GitHub Copilot CLI plugin marketplace**, making it easy to install the plugins it contains directly from the CLI.

---

## Plugins

### `fgerthoffert-personal`

A personal plugin containing:

| Skill | Description |
|---|---|
| [`writing-style`](./plugins/fgerthoffert-personal/skills/writing-style/SKILL.md) | Applies Francois Gerthoffert's personal writing style when generating or editing text. |
| [`marketplace-doctor`](./plugins/fgerthoffert-personal/skills/marketplace-doctor/SKILL.md) | Audits and fixes Copilot marketplace/plugin manifest issues so plugin installation and skill discovery work correctly. |

---

## Installation

### Install via marketplace

Register this repository as a Copilot CLI marketplace:

```sh
copilot plugin marketplace add Fgerthoffert/ai-harnesses
```

Browse available plugins:

```sh
copilot plugin marketplace browse ai-harnesses
```

Then install the personal plugin:

```sh
copilot plugin install fgerthoffert-personal@ai-harnesses
```

### Install directly

You can also install the plugin directly from the repository without registering the marketplace:

```sh
copilot plugin install Fgerthoffert/ai-harnesses
```

Or from the plugin subdirectory:

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

The plugin skills can then be invoked by name (for example `writing-style` or `marketplace-doctor`).

---

## Repository structure

```
.claude-plugin/
├── marketplace.json            # Primary marketplace manifest
└── plugin.json                 # Root plugin manifest (direct install)
.github/
└── plugin/
    └── marketplace.json        # Compatibility marketplace manifest
plugins/
└── fgerthoffert-personal/
    ├── plugin.json             # Plugin manifest
    └── skills/
        ├── marketplace-doctor/
        │   └── SKILL.md         # Marketplace diagnostics skill
        └── writing-style/
            └── SKILL.md         # Writing style skill
```
