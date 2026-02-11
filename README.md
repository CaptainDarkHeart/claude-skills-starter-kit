# Claude Skill Starter Kit

This starter kit contains everything you need to begin building Claude skills for your specific use cases.

## What's Included

- **complete-guide-to-building-skills-for-claude.md** - Full reference guide extracted from Anthropic's official documentation
- **SKILL-template.md** - Ready-to-use template for creating new skills
- **skill-project-structure.md** - Comprehensive guide to organizing your skill projects
- **example-skills/** - Working examples demonstrating different patterns

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

- **Official Skills Documentation**: https://docs.anthropic.com/claude/docs/skills
- **Example Skills Repository**: https://github.com/anthropics/skills
- **Claude Developers Discord**: For questions and support
- **skill-creator skill**: Use in Claude.ai to generate and review skills

## Tips from the Field

1. **Start with one use case** - Perfect one workflow before expanding
2. **Test trigger phrases** - Ask Claude "When would you use [skill-name]?"
3. **Use progressive disclosure** - Keep SKILL.md focused, details in references/
4. **Iterate based on real usage** - Skills are living documents
5. **Consider combining skills** - They work together, not in isolation

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
