# Contributing to Godot MMORPG

Thank you for your interest in contributing to the Godot MMORPG project! We welcome contributions from developers of all skill levels. This guide will help you get started.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Development Workflow](#development-workflow)
- [Coding Standards](#coding-standards)
- [Commit Guidelines](#commit-guidelines)
- [Pull Request Process](#pull-request-process)
- [Areas of Contribution](#areas-of-contribution)

## Code of Conduct

This project adheres to a [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to the project maintainers.

## Getting Started

### Prerequisites

- **Godot Engine 4.0+** - [Download here](https://godotengine.org/download)
- **Git** - For version control
- **Discord Account** - To join our community (optional but recommended)

### Setting Up Your Development Environment

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/GDMMORPG.git
   cd GDMMORPG
   ```
3. **Add upstream remote**:
   ```bash
   git remote add upstream https://github.com/GDMMORPG/GDMMORPG.git
   ```
4. **Open the project** in Godot Engine
5. **Join our Discord** to connect with other contributors

## How to Contribute

### Reporting Bugs

Before creating bug reports, please check the issue tracker to avoid duplicates. When creating a bug report, include:

- **Clear title and description**
- **Steps to reproduce** the issue
- **Expected behavior** vs actual behavior
- **Screenshots or videos** if applicable
- **Environment details** (OS, Godot version, etc.)

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, include:

- **Clear and descriptive title**
- **Detailed description** of the proposed feature
- **Rationale** - why this enhancement would be useful
- **Possible implementation** ideas (optional)

### Your First Code Contribution

Unsure where to begin? Look for issues labeled:

- `good first issue` - Simple issues perfect for beginners
- `help wanted` - Issues where we need community help
- `beginner-friendly` - Issues suitable for new contributors

## Development Workflow

1. **Create a new branch** for your feature or fix:
   ```bash
   git checkout -b feature/your-feature-name
   ```
   or
   ```bash
   git checkout -b fix/bug-description
   ```

2. **Make your changes** following our coding standards

3. **Test your changes** thoroughly in Godot

4. **Commit your changes** with clear, descriptive messages

5. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

6. **Open a Pull Request** against the `main` branch

## Coding Standards

### GDScript Style Guide

Follow the [official GDScript style guide](https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/gdscript_styleguide.html):

- **Indentation**: Use tabs (default in Godot)
- **Naming conventions**:
  - Variables and functions: `snake_case`
  - Constants: `UPPER_CASE`
  - Classes: `PascalCase`
  - Private variables/functions: prefix with `_`
- **Line length**: Keep lines under 100 characters when possible
- **Comments**: Use clear, concise comments to explain complex logic

Example:
```gdscript
extends CharacterBody2D

const MAX_HEALTH = 100
var current_health: int = MAX_HEALTH
var _is_dead: bool = false

func take_damage(amount: int) -> void:
    current_health -= amount
    if current_health <= 0:
        _die()

func _die() -> void:
    _is_dead = true
    queue_free()
```

### Project Organization

- Place scripts in appropriate directories (e.g., `scripts/player/`, `scripts/enemies/`)
- Keep scenes organized by type (e.g., `scenes/characters/`, `scenes/ui/`)
- Use clear, descriptive file names
- Group related assets together

## Commit Guidelines

### Commit Message Format

Follow the conventional commits format:

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

**Examples:**
```
feat(combat): add dodge roll mechanic

Implement dodge roll with i-frames and stamina cost.
Players can now dodge attacks using the dodge button.

Closes #123
```

```
fix(inventory): resolve item duplication bug

Fixed an issue where items could be duplicated by
rapidly clicking the split stack button.

Fixes #456
```

## Pull Request Process

1. **Update documentation** if you're changing functionality
2. **Add tests** if applicable
3. **Ensure your code follows** our coding standards
4. **Update the README.md** if you're adding new features
5. **Link related issues** in your PR description
6. **Request review** from maintainers
7. **Address feedback** promptly and professionally

### PR Title Format

Use the same format as commit messages:
- `feat(scope): description`
- `fix(scope): description`
- `docs: description`

### PR Description Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
How has this been tested?

## Screenshots (if applicable)
Add screenshots for visual changes

## Checklist
- [ ] Code follows project style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex code
- [ ] Documentation updated
- [ ] No new warnings generated
- [ ] Tests added/updated
```

## Areas of Contribution

### Programming

- **Gameplay Systems**: Combat, inventory, quests, progression
- **Networking**: Multiplayer synchronization, server architecture
- **UI/UX**: Menus, HUDs, interfaces
- **AI**: NPC behavior, enemy AI
- **Tools**: Editor extensions, debugging tools

### Art & Design

- **3D Assets**: Characters, environments, props
- **2D Assets**: UI elements, icons, textures
- **Animation**: Character animations, VFX
- **Level Design**: World building, dungeons

### Audio

- **Music**: Background tracks, combat themes
- **SFX**: Combat sounds, ambient audio, UI sounds
- **Audio Implementation**: Integrating audio into the game

### Game Design

- **Systems Design**: Balance, mechanics, progression
- **Content Creation**: Quests, lore, dialogue
- **Level Design**: Encounters, puzzles, exploration

### Documentation

- **Code Documentation**: Inline comments, API docs
- **User Documentation**: Guides, tutorials, wiki
- **Process Documentation**: Development workflows, standards

## Questions?

- **Discord**: Join our server for real-time help
- **GitHub Discussions**: For longer-form questions
- **Issues**: For bug reports and feature requests

## Recognition

All contributors will be recognized in:
- The project's [Contributors](../../graphs/contributors) page
- Release notes for significant contributions
- Our community hall of fame

Thank you for contributing to Godot MMORPG! 🎮
