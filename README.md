# AI Architect Plugin

A minimal, production-grade Claude Code plugin for generating consistent, high-quality system designs.

## Features

- **`/design-system` command**: Generates a deterministic system design document.
- Follows strict engineering rules defined in `skills/architecture-patterns.md`.
- Enforces an exact structural layout via `templates/system-design-template.md`.

## Installation (Local)

1. Clone this repository:
   ```bash
   git clone <your-repo-url>
   cd ai-architect-plugin
   ```
2. Open Claude Code and install the plugin from the local path:
   ```bash
   # In Claude Code, install the plugin from the local directory
   # Ensure you are at the root of the ai-architect-plugin folder
   ```

## Usage

In Claude Code, invoke the `/design-system` command:

```
/design-system I need an event-driven architecture for a real-time chat application.
```

## Structure

```
ai-architect-plugin/
  .claude-plugin/
    plugin.json               # Plugin configuration
  commands/
    design-system.md          # Command definition
  skills/
    architecture-patterns.md  # Engineering rules and architectural patterns
  templates/
    system-design-template.md # Structural template for outputs
```

## Version

v0.1.0
