# Getting Started with Claude Skills

Welcome! This guide will get you building your first Claude skill in 15-30 minutes.

## What You Have

This starter kit contains:

1. **complete-guide-to-building-skills-for-claude.md** - Complete reference (33 pages)
2. **SKILL-template.md** - Copy this to start any new skill
3. **skill-project-structure.md** - File organization patterns
4. **example-skills/simple-example/** - Working example you can test
5. **This file** - Quick start guide

## Your First Skill in 5 Steps

### Step 1: Understand What Skills Are (2 minutes)

A skill is just a folder with a `SKILL.md` file that teaches Claude how to do something specific.

**Three-level system:**
- **Level 1** (YAML frontmatter) - Always loaded, tells Claude when to use the skill
- **Level 2** (SKILL.md body) - Loaded when relevant, contains instructions
- **Level 3** (Other files) - Loaded on-demand for details

### Step 2: Choose Your Use Case (3 minutes)

Pick ONE thing you do repeatedly that could be automated:

**Examples:**
- Create weekly status reports in a specific format
- Summarize meeting transcripts with action items
- Generate code following your team's style guide
- Set up new projects with standard structure
- Review documents for compliance requirements

**Your use case:**
> [Write it here before continuing]

### Step 3: Create Your Skill (10 minutes)

```bash
# 1. Create a folder (use kebab-case)
mkdir my-first-skill

# 2. Copy the template
cp SKILL-template.md my-first-skill/SKILL.md

# 3. Edit the frontmatter
# Change these fields:
#   - name: my-first-skill
#   - description: [what it does] Use when user [trigger phrases]

# 4. Write 3-5 clear steps in the Instructions section

# 5. Add 1-2 examples of how it works
```

**Key tips:**
- Make the description SPECIFIC with trigger phrases users would actually say
- Keep instructions clear and actionable
- Include at least one complete example

### Step 4: Test Your Skill (5 minutes)

```bash
# 1. Zip your skill folder
cd ..
zip -r my-first-skill.zip my-first-skill/

# 2. Upload to Claude.ai
#    - Open Claude.ai
#    - Go to Settings > Capabilities > Skills
#    - Click "Upload skill"
#    - Select your .zip file

# 3. Test with queries that should trigger it
#    - Use the exact phrases from your description
#    - Try paraphrased versions
#    - Try unrelated queries (should NOT trigger)
```

### Step 5: Iterate (10+ minutes)

Based on testing:

**If skill doesn't trigger:**
- Add more trigger phrases to description
- Make description more specific
- Include file types if relevant

**If skill triggers but instructions unclear:**
- Add more detail to steps
- Include error handling
- Add more examples

**If skill triggers on wrong queries:**
- Make description more specific
- Add negative triggers ("Do NOT use for...")
- Narrow the scope

## Testing Checklist

Run through these before sharing your skill:

- [ ] Triggers on 3+ different phrasings of the same request
- [ ] Doesn't trigger on unrelated requests
- [ ] Produces consistent output across runs
- [ ] Handles errors gracefully
- [ ] Instructions are clear without needing clarification

## Common Mistakes to Avoid

❌ **Too vague:** "Helps with documents"
✅ **Specific:** "Creates executive summaries of meeting transcripts with action items"

❌ **No triggers:** "Sophisticated analysis tool"
✅ **Clear triggers:** "Use when user uploads CSV and asks for 'statistical analysis' or 'data insights'"

❌ **Kitchen sink:** Trying to do 10 different things
✅ **Focused:** Does one thing really well

❌ **Giant SKILL.md:** Everything in one file
✅ **Progressive disclosure:** Core in SKILL.md, details in references/

## Next Steps After Your First Skill

1. **Add scripts/** if you need validation or processing logic
2. **Add references/** for detailed documentation
3. **Add assets/** for templates or resources
4. **Create variations** for related workflows
5. **Share with team** and gather feedback

## Quick Reference

### File Structure
```
my-skill/
├── SKILL.md          # Required
├── scripts/          # Optional - Python, Bash, etc.
├── references/       # Optional - Detailed docs
└── assets/           # Optional - Templates, images
```

### YAML Frontmatter Minimum
```yaml
---
name: my-skill-name
description: What it does. Use when [triggers].
---
```

### Description Formula
```
[What] + [When to use it] + [Key capabilities]
```

### Good Trigger Phrases
- Specific actions: "summarize", "create report", "analyze data"
- File types: "uploads CSV", "PDF document", ".docx file"  
- Keywords: "sprint planning", "code review", "compliance check"

## Where to Get Help

1. **Read the guide:** `complete-guide-to-building-skills-for-claude.md`
2. **Check structures:** `skill-project-structure.md`
3. **Review example:** `example-skills/simple-example/SKILL.md`
4. **Use skill-creator:** In Claude.ai, say "Use skill-creator to help me build a skill"
5. **Ask community:** Claude Developers Discord

## Real Talk: What Makes Skills Work

The best skills come from:
- ✅ Real problems you face repeatedly
- ✅ Clear, specific workflows you can document
- ✅ Trigger phrases people naturally use
- ✅ Starting simple and iterating

Not from:
- ❌ Trying to be clever or impressive
- ❌ Building before you understand the workflow
- ❌ Over-engineering on day one
- ❌ Vague, generic descriptions

## Your Action Plan

Right now, before doing anything else:

1. [ ] Pick ONE specific use case you actually need
2. [ ] Write down 3 trigger phrases users would say
3. [ ] List the 5 steps in the workflow
4. [ ] Copy the template and fill it in
5. [ ] Test it with real queries
6. [ ] Iterate based on what works

**Time estimate:** 15-30 minutes for a working first version.

Then improve it over time as you use it.

---

**Remember:** Perfect is the enemy of shipped. Build something that works, then make it better.

Ready? Let's build. 🚀
