# Repository Structure

This document explains the organization of Local LLM Cookbook, the purpose of its directories, and where different types of documentation, examples, configurations, and scripts belong.

## Project Architecture

```text
local-llm-cookbook/
│
├── .github/                  # GitHub templates and automation
│   ├── ISSUE_TEMPLATE/       # Issue templates
│   └── workflows/            # CI workflows
│
├── assets/                   # Project images and visual assets
│
├── configs/                  # Reusable configurations
│   └── training/             # Model training configurations
│
├── docs/                     # Core project documentation
│
├── examples/                 # Practical code examples
│   ├── datasets/             # Sample datasets
│   ├── inference/            # Local inference examples
│   ├── fine-tuning/          # Fine-tuning examples
│   └── deployment/           # Model deployment examples
│
├── guides/                   # Step-by-step tutorials
│   ├── running-local-llms/   # Local model execution
│   ├── fine-tuning/          # Fine-tuning workflows
│   └── deployment/           # Model conversion and deployment
│
├── scripts/                  # Setup and utility scripts
│
├── tests/                    # Automated tests
│
├── .editorconfig             # Editor configuration
├── .gitignore                # Git ignore rules
├── .pre-commit-config.yaml   # Pre-commit configuration
├── CHANGELOG.md              # Project change history
├── CODE_OF_CONDUCT.md        # Community standards
├── CONTRIBUTING.md           # Contribution guidelines
├── LICENSE                   # Project license
├── pyproject.toml            # Python project configuration
├── README.md                 # Project introduction
├── requirements.txt          # Python dependencies
├── SECURITY.md               # Security policy
└── SUPPORT.md                # Support information
```

## Directory Responsibilities

### `.github/`

Contains GitHub-specific configuration, issue templates, pull request templates, and automated workflows.

### `assets/`

Stores project branding and visual resources, including the repository logo and documentation images.

### `configs/`

Contains reusable configuration files for experiments and training workflows.

### `docs/`

Contains foundational documentation covering hardware requirements, model selection, quantization, terminology, setup, and troubleshooting.

### `examples/`

Contains practical and reproducible code examples.

Each example should include relevant dependencies, execution instructions, and hardware assumptions where applicable.

### `guides/`

Contains detailed tutorials organized by workflow and tool.

Examples include running models with Ollama or LM Studio, fine-tuning with Unsloth or LLaMA-Factory, and exporting models to GGUF.

### `scripts/`

Contains utilities for environment setup, dependency checks, and development workflows.

### `tests/`

Contains automated tests for example code, datasets, and configuration validation.

## Root-Level Files

| File | Purpose |
|---|---|
| `README.md` | Project overview and navigation |
| `LICENSE` | Open-source licensing terms |
| `CONTRIBUTING.md` | Contribution process |
| `CODE_OF_CONDUCT.md` | Community expectations |
| `SECURITY.md` | Vulnerability reporting |
| `SUPPORT.md` | Help and support information |
| `CHANGELOG.md` | Version history |
| `pyproject.toml` | Python project configuration |
| `requirements.txt` | Python dependencies |
| `.gitignore` | Files excluded from Git |
| `.editorconfig` | Consistent editor settings |
| `.pre-commit-config.yaml` | Pre-commit checks |

## Organization Principles

The repository follows a few simple principles:

1. Keep foundational documentation separate from practical tutorials.
2. Keep runnable code inside `examples/`.
3. Keep reusable configurations inside `configs/`.
4. Organize guides by workflow rather than duplicating documentation.
5. Include clear execution instructions and hardware requirements.
6. Avoid unnecessary abstractions and premature complexity.

## Adding New Content

Before adding a new file, consider its purpose:

- General concepts and reference material belong in `docs/`.
- Step-by-step workflows belong in `guides/`.
- Runnable code belongs in `examples/`.
- Reusable settings belong in `configs/`.
- Development utilities belong in `scripts/`.
- Automated checks belong in `tests/`.

The goal is to keep Local LLM Cookbook easy to navigate, maintain, and extend as the project grows.