# Python Module 06 — The Alchemist's Codex

> **42 School Project - Python Module 06**  
> Mastering Python's Import Mysteries through alchemical experiments.

---

## 🚀 Overview

This repository contains the solutions for **Python Module 06**, focused on mastering Python's import system. Through the theme of an Alchemical Laboratory, the project explores the four sacred mysteries of Python imports: package initialization, import pathways, absolute vs relative imports, and circular dependency resolution.

---

## 📝 Project Objectives

- Understand how `__init__.py` transforms folders into Python packages
- Control package interfaces (what's exposed vs what's hidden)
- Master different import styles: `import`, `from...import`, `import...as`
- Distinguish between absolute and relative imports
- Identify and resolve circular dependencies using late imports

---

## 📁 Repository Structure

```
.
├── ft_sacred_scroll.py              # Part I  - Demo script
├── ft_import_transmutation.py       # Part II - Demo script
├── ft_pathway_debate.py             # Part III - Demo script
├── ft_circular_curse.py             # Part IV - Demo script
├── alchemy/
│   ├── __init__.py                  # Sacred Scroll (package initializer)
│   ├── elements.py                  # Basic elemental spells
│   ├── potions.py                   # Advanced potion recipes
│   ├── transmutation/
│   │   ├── __init__.py              # Transmutation package initializer
│   │   ├── basic.py                 # Absolute imports demo
│   │   └── advanced.py             # Relative imports demo
│   └── grimoire/
│       ├── __init__.py              # Grimoire package initializer
│       ├── spellbook.py             # Late import (circular fix)
│       └── validator.py             # Ingredient validation
└── README.md
```

---

## 🧪 The Four Sacred Mysteries

### Part I — The Sacred Scroll (`__init__.py`)
Discover how `__init__.py` controls which functions are exposed at package level. Only `create_fire` and `create_water` are accessible via `alchemy.function()`, while `create_earth` and `create_air` remain hidden.

### Part II — Import Transmutation (`from...import`)
Master four import styles: full module import, specific function import, aliased import (`as`), and multiple imports. Each method has different trade-offs.

### Part III — The Great Pathway Debate (Absolute vs Relative)
`basic.py` uses **absolute imports** (`from alchemy.elements import ...`) while `advanced.py` uses **relative imports** (`from .basic import ...`, `from ..potions import ...`). Both achieve the same result with different approaches.

### Part IV — Breaking the Circular Curse
`spellbook.py` uses a **late import** (import inside the function body) to avoid circular dependencies with `validator.py`.

---

## 🚦 Usage

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd PythonModule06
   ```

2. **Run each part**
   ```bash
   python3 ft_sacred_scroll.py
   python3 ft_import_transmutation.py
   python3 ft_pathway_debate.py
   python3 ft_circular_curse.py
   ```

---

## 📚 General Instructions

- Written in **Python 3.10+**
- **No external libraries** — only Python standard library
- All functions return **strings**
- Errors handled gracefully with `try/except` returning descriptive messages
- **Forbidden**: `eval()`, `exec()`, `sys.path` modification, `importlib`

---

## ✅ Requirements

- Python 3.x
- No `pip install` needed — zero external dependencies

---

## 🔍 Evaluation

During defense, you may be asked to:
- Run each of the 4 scripts and verify correct output
- Explain how `__init__.py` controls package exposure
- Explain the difference between absolute and relative imports
- Explain what circular dependencies are and how late imports solve them
- Modify the laboratory live (add functions, change import styles)

---

## 💡 Key Concepts

| Concept | File | Technique |
|---|---|---|
| Package init | `alchemy/__init__.py` | `from .elements import create_fire, create_water` |
| Hidden functions | `elements.py` | `create_earth`/`create_air` not in `__init__.py` |
| Absolute import | `transmutation/basic.py` | `from alchemy.elements import create_fire` |
| Relative import | `transmutation/advanced.py` | `from .basic import lead_to_gold` |
| Parent relative | `transmutation/advanced.py` | `from ..potions import healing_potion` |
| Late import | `grimoire/spellbook.py` | `from .validator import validate_ingredients` inside function |

---

## 📄 License

This project is part of the **42 School** curriculum and is intended for educational use.

---

## 🏫 42 School

> *"Learning to learn."*  
> Code, share, and grow together.

