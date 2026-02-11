# Claude Skill Project Structure Guide

This guide provides recommended project structures for different types of Claude skills.

## Basic Skill Structure

The minimal structure for any skill:

```
your-skill-name/
├── SKILL.md              # Required: Main skill file with YAML frontmatter
└── README.md             # Optional: For GitHub/distribution (NOT included in skill folder when uploading)
```

## Standard Skill Structure (Recommended)

A well-organized skill with common optional components:

```
your-skill-name/
├── SKILL.md              # Required: Main instructions
├── scripts/              # Optional: Executable code
│   ├── validate.py       # Validation scripts
│   ├── process.py        # Processing logic
│   └── utils.sh          # Helper utilities
├── references/           # Optional: Extended documentation
│   ├── api-guide.md      # API reference
│   ├── best-practices.md # Usage guidelines
│   └── examples/         # Example files
│       ├── example-1.md
│       └── example-2.md
└── assets/               # Optional: Templates and resources
    ├── templates/
    │   ├── report-template.md
    │   └── email-template.txt
    └── icons/
        └── skill-icon.png
```

## MCP-Enhanced Skill Structure

For skills that coordinate with MCP servers:

```
your-mcp-skill/
├── SKILL.md              # Main instructions with MCP workflows
├── scripts/
│   ├── mcp-test.py       # Test MCP connectivity
│   ├── validate-auth.py  # Check MCP authentication
│   └── error-handler.py  # MCP error recovery
├── references/
│   ├── mcp-setup.md      # MCP configuration guide
│   ├── api-patterns.md   # Common MCP call patterns
│   ├── error-codes.md    # MCP error reference
│   └── workflows/
│       ├── workflow-1.md # Detailed workflow docs
│       └── workflow-2.md
└── assets/
    └── mcp-config-template.json
```

## Document Creation Skill Structure

For skills focused on creating documents (PDF, DOCX, PPTX, etc.):

```
doc-creation-skill/
├── SKILL.md              # Document creation instructions
├── scripts/
│   ├── format-checker.py # Validate output format
│   └── style-applier.py  # Apply styling rules
├── references/
│   ├── style-guide.md    # Brand/style standards
│   ├── formatting-rules.md
│   └── examples/
│       ├── sample-doc.md
│       ├── sample-report.md
│       └── sample-presentation.md
└── assets/
    ├── templates/
    │   ├── report-template.docx
    │   ├── presentation-template.pptx
    │   └── spreadsheet-template.xlsx
    ├── fonts/
    │   └── custom-font.ttf
    ├── images/
    │   ├── logo.png
    │   └── brand-assets/
    └── styles/
        └── style-definitions.json
```

## Multi-MCP Coordination Skill Structure

For skills that orchestrate multiple MCP servers:

```
multi-mcp-orchestrator/
├── SKILL.md              # Orchestration instructions
├── scripts/
│   ├── orchestrator.py   # Main coordination logic
│   ├── mcp-router.py     # Route to appropriate MCP
│   └── state-manager.py  # Track workflow state
├── references/
│   ├── mcp-integrations/
│   │   ├── figma-mcp.md
│   │   ├── linear-mcp.md
│   │   ├── github-mcp.md
│   │   └── slack-mcp.md
│   ├── workflows/
│   │   ├── design-handoff.md
│   │   ├── project-setup.md
│   │   └── deployment-flow.md
│   └── coordination-patterns.md
└── assets/
    └── workflow-diagrams/
        ├── full-workflow.png
        └── error-handling.png
```

## Complex Workflow Automation Skill Structure

For sophisticated multi-step automation:

```
workflow-automation-skill/
├── SKILL.md              # High-level workflow instructions
├── scripts/
│   ├── workflow-engine.py    # Core workflow execution
│   ├── validators/
│   │   ├── input-validator.py
│   │   ├── step-validator.py
│   │   └── output-validator.py
│   ├── processors/
│   │   ├── data-processor.py
│   │   ├── api-handler.py
│   │   └── file-handler.py
│   └── utils/
│       ├── logging.py
│       └── error-recovery.py
├── references/
│   ├── architecture.md       # System design docs
│   ├── workflows/
│   │   ├── workflow-spec-1.md
│   │   ├── workflow-spec-2.md
│   │   └── workflow-spec-3.md
│   ├── api-reference/
│   │   ├── endpoints.md
│   │   └── data-models.md
│   └── troubleshooting/
│       ├── common-issues.md
│       └── debug-guide.md
└── assets/
    ├── config/
    │   ├── default-config.json
    │   └── environment-vars.example
    ├── templates/
    │   ├── input-template.json
    │   └── output-template.json
    └── schemas/
        ├── input-schema.json
        └── output-schema.json
```

## GitHub Distribution Structure

When hosting your skill on GitHub for distribution:

```
your-skill-repo/
├── README.md             # For GitHub visitors (installation, usage)
├── LICENSE               # Open source license
├── .gitignore
├── CHANGELOG.md
├── your-skill-name/      # ← The actual skill folder
│   ├── SKILL.md          # NO README.md inside here
│   ├── scripts/
│   ├── references/
│   └── assets/
├── tests/                # Test suite (outside skill folder)
│   ├── test-triggers.md
│   ├── test-functional.md
│   └── test-cases/
├── docs/                 # Extended documentation (outside skill folder)
│   ├── installation.md
│   ├── configuration.md
│   ├── examples.md
│   └── api-reference.md
└── examples/             # Usage examples (outside skill folder)
    ├── example-1/
    └── example-2/
```

## Key Structure Rules

### ✅ DO:
- Name skill folder in `kebab-case`
- Use exactly `SKILL.md` (case-sensitive)
- Organize scripts by function
- Keep SKILL.md focused and concise
- Move detailed docs to `references/`
- Use descriptive folder and file names

### ❌ DON'T:
- Include `README.md` inside the skill folder
- Use spaces or capitals in folder names
- Put all instructions in SKILL.md (use progressive disclosure)
- Include sensitive data or credentials
- Use platform-specific paths (keep portable)

## File Naming Conventions

```
Good:
✅ validate-input.py
✅ api-handler.js
✅ report-template.docx
✅ workflow-guide.md

Bad:
❌ Validate Input.py         (spaces)
❌ APIHandler.js              (camelCase)
❌ Report_Template.docx       (underscores in assets)
❌ workflow guide.md          (spaces)
```

## Progressive Disclosure Strategy

Structure your skill to load information progressively:

**Level 1 (Always loaded):** YAML frontmatter in SKILL.md
```yaml
---
name: your-skill
description: What and when to use it
---
```

**Level 2 (Loaded when relevant):** Main SKILL.md body
- Core instructions
- Common workflows
- Essential examples
- Links to level 3

**Level 3 (Loaded on-demand):** References and assets
- `references/detailed-api-guide.md`
- `references/advanced-patterns.md`
- `assets/templates/`

## Testing Structure

Recommended test organization (outside skill folder):

```
tests/
├── unit/
│   ├── test-scripts.py       # Test individual scripts
│   └── test-validators.py
├── integration/
│   ├── test-mcp-calls.py     # Test MCP integration
│   └── test-workflows.py
├── trigger-tests/
│   ├── should-trigger.md     # Queries that should activate skill
│   └── should-not-trigger.md # Queries that shouldn't
└── functional-tests/
    ├── test-case-1.md
    ├── test-case-2.md
    └── test-case-3.md
```

## Size Guidelines

To maintain performance and usability:

- **SKILL.md:** Target < 5,000 words
- **References:** Individual files < 3,000 words
- **Scripts:** Keep modular and focused
- **Assets:** Optimize file sizes (compress images, etc.)
- **Total skill size:** Aim for < 5MB when zipped

## Example: Minimal Working Skill

The absolute minimum to get started:

```
simple-skill/
└── SKILL.md
```

With content:
```yaml
---
name: simple-skill
description: Does X when user asks to Y
---

# Simple Skill

## Instructions

1. Do this first
2. Then do this
3. Finally do this

## Example

User says: "Do Y"
Result: X is created
```

That's it! You can always expand from here.

## Quick Start Checklist

- [ ] Create folder with `kebab-case` name
- [ ] Create `SKILL.md` with frontmatter
- [ ] Write clear description with triggers
- [ ] Add core instructions
- [ ] Test with basic queries
- [ ] Add `scripts/` if needed
- [ ] Add `references/` for detailed docs
- [ ] Add `assets/` for templates/resources
- [ ] Zip folder for upload
- [ ] Test in Claude

---

**Pro Tip:** Start minimal, iterate based on usage. Don't over-engineer on day one.
