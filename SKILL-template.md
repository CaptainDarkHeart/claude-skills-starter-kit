---
name: your-skill-name
description: [What your skill does]. Use when user asks to [specific trigger phrases], mentions [key terms], or uploads [relevant file types].
license: MIT
metadata:
  author: Your Name/Company
  version: 1.0.0
  mcp-server: your-mcp-server-name # Optional: if this skill enhances an MCP
  category: [productivity|development|content|automation]
  tags: [tag1, tag2, tag3]
---

# Your Skill Name

[Brief 1-2 sentence overview of what this skill does and why it's valuable]

## Instructions

### Step 1: [First Major Action]

[Clear explanation of what happens in this step]

**Example:**
```bash
# If using scripts
python scripts/your_script.py --param value
```

**Expected output:** [Describe what success looks like]

**Key considerations:**
- [Important point 1]
- [Important point 2]

### Step 2: [Second Major Action]

[Explanation of this step and how it builds on Step 1]

**MCP calls:** (if applicable)
- Tool: `tool_name`
- Parameters: `param1`, `param2`
- Returns: [What data comes back]

### Step 3: [Subsequent Steps]

[Continue with additional steps as needed]

## Workflow Overview

For complex multi-step processes, provide a visual overview:

```
1. [Initial Step] → 2. [Processing] → 3. [Validation] → 4. [Output]
     ↓                                      ↓
  [Error handling]              [Refinement loop if needed]
```

## Examples

### Example 1: [Common Use Case]

**User says:** "[Natural language request]"

**What the skill does:**
1. [Action 1]
2. [Action 2]
3. [Action 3]

**Result:** [What the user gets]

### Example 2: [Another Use Case]

**User says:** "[Different request style]"

**What the skill does:**
1. [Different workflow]
2. [Based on context]

**Result:** [Different outcome]

### Example 3: [Edge Case or Advanced Usage]

**User says:** "[Complex request]"

**What the skill does:**
1. [Handle complexity]
2. [Multiple sub-steps]

**Result:** [Advanced outcome]

## Quality Standards

Before finalizing output, verify:

- [ ] [Quality check 1]
- [ ] [Quality check 2]
- [ ] [Quality check 3]
- [ ] [All required fields present]
- [ ] [Format matches requirements]

## Error Handling

### Error: [Common Error Message]

**Cause:** [Why this happens]

**Solution:**
1. [Step to resolve]
2. [Alternative approach if needed]
3. [How to verify fix worked]

### Error: [Another Common Error]

**Cause:** [Root cause]

**Solution:**
- [Quick fix approach]
- [When to escalate]

### MCP Connection Issues (if applicable)

If MCP calls fail:

1. **Verify connection:** Settings > Extensions > [Service Name]
2. **Check authentication:** Ensure API key/token is valid
3. **Test independently:** Try calling MCP tool directly without skill
4. **Review logs:** Check for specific error codes

## Troubleshooting

### Problem: [Common Issue]

**Symptoms:**
- [What user sees]
- [Unexpected behavior]

**Diagnosis:**
1. [Check this first]
2. [Then check this]

**Resolution:**
- [Solution steps]

### Problem: [Another Issue]

**Quick fixes:**
- [Try this first]
- [Or this alternative]

## Best Practices

When using this skill:

1. **[Best Practice 1]** - [Why this matters]
2. **[Best Practice 2]** - [What to avoid]
3. **[Best Practice 3]** - [Optimization tip]

## Advanced Usage

### Combining with Other Skills

This skill works well alongside:
- **[skill-name]** - [How they complement each other]
- **[another-skill]** - [Combined workflow benefits]

### Customization Options

You can customize behavior by:
- [Configuration option 1]
- [Configuration option 2]
- Modifying `references/config.md` for [specific customizations]

## Reference Materials

For detailed information, see:
- `references/api-guide.md` - [What's documented there]
- `references/examples/` - [Sample files and templates]
- `assets/template.md` - [Template files used by this skill]

## Performance Notes

- Expected completion time: [X minutes/seconds]
- Token usage: [Approximate range]
- MCP calls: [Typical number]
- Works best when: [Optimal conditions]

## Limitations

Current limitations:
- [What this skill doesn't do]
- [Known constraints]
- [Future enhancements planned]

## Version History

### v1.0.0 (Current)
- Initial release
- [Key feature 1]
- [Key feature 2]

---

**Support:** [Contact information or issue tracker]
**Documentation:** [Link to fuller docs if available]
**License:** [License type from frontmatter]
