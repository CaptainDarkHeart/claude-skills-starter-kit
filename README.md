# Claude Skills Starter Kit

> **Note:** This repository is a community resource for building skills for Claude. For the official Agent Skills standard and specification, see [agentskills.io](https://agentskills.io). For Anthropic's example skills, see [anthropics/skills](https://github.com/anthropics/skills).

A comprehensive starter kit containing everything you need to begin building Claude skills for your specific use cases.

## What Are Skills?

Skills are folders of instructions, scripts, and resources that Claude loads dynamically to improve performance on specialized tasks. They teach Claude how to complete specific tasks in a repeatable way—whether that's creating documents with your company's brand guidelines, analyzing data using your organization's workflows, or automating personal tasks.

**Learn more:**
- [What are skills?](https://support.claude.com/en/articles/12512176-what-are-skills)
- [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude)
- [Creating custom skills](https://support.claude.com/en/articles/12512198-creating-custom-skills)
- [Agent Skills Standard](https://agentskills.io/specification)

## What's Included

- **complete-guide-to-building-skills-for-claude.md** - Full reference guide extracted from Anthropic's official documentation
- **SKILL-template.md** - Minimal template for creating new skills
- **skill-project-structure.md** - Comprehensive guide to organizing your skill projects
- **GETTING-STARTED.md** - Step-by-step tutorial for building your first skill

## Quick Start

### 1. Choose Your Skill Type

Decide what you want to build:
- **Document Creation** - Generate consistent documents, presentations, spreadsheets
- **Workflow Automation** - Multi-step processes with validation
- **MCP Enhancement** - Add expertise layer to your MCP server
- **Multi-MCP Coordination** - Orchestrate workflows across services

### 2. Copy the Template

```bash
cp SKILL-template.md your-skill-name/SKILL.md
```

### 3. Fill in Your Details

Edit the YAML frontmatter:
```yaml
---
name: your-skill-name  # kebab-case only
description: What it does. Use when user [trigger phrases].
---
```

### 4. Write Instructions

Follow the template structure or reference the patterns in the complete guide.

### 5. Test Your Skill

1. Zip your skill folder
2. Upload to Claude.ai: Settings > Capabilities > Skills
3. Test with relevant queries
4. Iterate based on results

## File Structure Quick Reference

### Minimal (Start Here)
```
your-skill/
└── SKILL.md
```

### Standard
```
your-skill/
├── SKILL.md
├── scripts/
├── references/
└── assets/
```

### For Distribution
```
your-skill-repo/
├── README.md          # For GitHub
├── LICENSE
├── your-skill/        # The actual skill
│   └── SKILL.md
└── tests/
```

## Key Rules to Remember

✅ **DO:**
- Use `kebab-case` for folder names
- Name file exactly `SKILL.md` (case-sensitive)
- Include trigger phrases in description
- Start minimal, iterate based on usage

❌ **DON'T:**
- Put README.md inside skill folder
- Use spaces or capitals in names
- Include XML tags (< >) in frontmatter
- Over-engineer on day one

## Common Patterns

### Pattern 1: Sequential Workflow
Step-by-step processes in specific order

### Pattern 2: Multi-MCP Coordination
Orchestrating multiple services together

### Pattern 3: Iterative Refinement
Output that improves through iteration

### Pattern 4: Context-Aware Selection
Choose right tools based on context

### Pattern 5: Domain Intelligence
Add specialized expertise beyond tool access

See `complete-guide-to-building-skills-for-claude.md` Chapter 5 for detailed examples.

## Testing Checklist

- [ ] Triggers on relevant queries
- [ ] Doesn't trigger on unrelated queries
- [ ] Produces expected outputs
- [ ] Handles errors gracefully
- [ ] Performs better than baseline

## Resources

- **Agent Skills Standard**: https://agentskills.io
- **Official Skills Documentation**: https://docs.anthropic.com/claude/docs/skills
- **Anthropic Example Skills**: https://github.com/anthropics/skills
- **Claude Support**: https://support.claude.com
- **skill-creator skill**: Use in Claude.ai to generate and review skills

## Core Principles

1. **Concise is Key** - The context window is a public good. Only add context Claude doesn't already have.
2. **Start with one use case** - Perfect one workflow before expanding
3. **Test trigger phrases** - Ask Claude "When would you use [skill-name]?"
4. **Use progressive disclosure** - Keep SKILL.md focused, details in references/
5. **Iterate based on real usage** - Skills are living documents
6. **Assume Claude is smart** - Don't over-explain what Claude already knows

## Getting Help

- Review the complete guide for detailed explanations
- Check troubleshooting section for common issues
- Use skill-creator in Claude.ai for generation and review
- Post questions in Claude Developers Discord

## Next Steps

1. Read through `complete-guide-to-building-skills-for-claude.md`
2. Review `skill-project-structure.md` for your use case
3. Copy and customize `SKILL-template.md`
4. Build your first skill in 15-30 minutes
5. Test, iterate, and refine

---

**Remember:** The best skills solve real problems you encounter repeatedly. Start with what you actually need, not what sounds impressive.
