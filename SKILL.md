---
name: content-summarizer
description: Creates concise summaries of long-form content including articles, documents, and reports. Use when user asks to "summarize", "create a summary", "give me the key points", or uploads documents for summarization.
license: MIT
metadata:
  author: Example Author
  version: 1.0.0
  category: productivity
  tags: [summarization, content, productivity]
---

# Content Summarizer

Creates structured, concise summaries of long-form content while preserving key information and context.

## Instructions

### Step 1: Analyze the Content

Read through the provided content and identify:
- Main topic and purpose
- Key arguments or findings
- Supporting evidence
- Conclusions or recommendations

### Step 2: Structure the Summary

Organize the summary using this format:

**Overview** (1-2 sentences)
- The big picture - what is this about?

**Key Points** (3-5 bullet points)
- Most important takeaways
- Main arguments or findings

**Details** (optional, if requested)
- Supporting information
- Notable quotes or data
- Context that matters

**Conclusion** (1 sentence)
- The bottom line

### Step 3: Validate Quality

Before finalizing, ensure:
- [ ] Summary is 20-30% of original length
- [ ] No critical information lost
- [ ] Written clearly and concisely
- [ ] Maintains objective tone
- [ ] Free of jargon unless essential

## Examples

### Example 1: Article Summary

**User says:** "Summarize this article about remote work trends"

**What the skill does:**
1. Reads article content
2. Identifies main theme (remote work evolution)
3. Extracts key statistics and trends
4. Creates structured summary with overview, key points, conclusion

**Result:** 
```
Overview: Article examines how remote work has evolved from emergency 
measure to permanent fixture in modern business.

Key Points:
• 73% of companies now offer hybrid work options, up from 12% in 2019
• Employee satisfaction increased 35% with flexible arrangements
• Challenges include collaboration tools and maintaining company culture
• Companies saving average of $11,000/year per remote employee

Conclusion: Remote work is now integral to talent retention and 
operational efficiency.
```

### Example 2: Document Summary

**User says:** "Give me the key points from this meeting transcript"

**What the skill does:**
1. Processes transcript
2. Identifies decisions made
3. Notes action items
4. Summarizes discussions

**Result:** Structured summary with decisions, action items, and next steps

## Quality Standards

Summaries should be:
- **Accurate** - No misrepresentation of source material
- **Concise** - Typically 20-30% of original length
- **Objective** - Neutral tone without injecting opinions
- **Complete** - All critical information preserved
- **Clear** - Easily understood by someone who hasn't read the original

## Troubleshooting

### Problem: Summary too long

**Solution:**
- Focus on main points only
- Remove redundant information
- Eliminate examples unless crucial
- Target 20-30% of original length

### Problem: Missing important context

**Solution:**
- Re-read with focus on "why" not just "what"
- Include essential background information
- Note key relationships between concepts

### Problem: Too much detail

**Solution:**
- Ask: "Would someone need this to understand the core message?"
- Keep statistics only if they're central to the argument
- Save deep details for "Details" section if requested

## Best Practices

1. **Read once completely before summarizing** - Get the full picture first
2. **Use the author's language for key terms** - Maintain accuracy
3. **Preserve the logical flow** - Don't just list facts randomly
4. **Note the intended audience** - Adjust complexity accordingly
5. **Include source context** - Date, author, publication when relevant

## Limitations

This skill works best for:
- Text-based content (articles, documents, reports)
- Lengths from 500 to 10,000 words
- Non-technical to moderately technical content

May require adjustment for:
- Highly specialized technical papers
- Content requiring domain expertise to evaluate
- Multi-media content with essential visual elements
