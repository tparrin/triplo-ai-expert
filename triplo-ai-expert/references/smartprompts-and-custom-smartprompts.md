# SmartPrompts and Custom SmartPrompts

## What are SmartPrompts?

SmartPrompts are **reusable prompt templates** that ensure consistent, high-quality AI outputs for specific tasks. They encode instructions so the AI behaves predictably every time you use them.

### Key Benefits

| Benefit | Why It Matters |
|---------|----------------|
| **Consistency** | Same prompt structure every time |
| **Quality** | Pre-tested, optimized instructions |
| **Efficiency** | One-click execution, no typing |
| **Shareability** | Can be shared across teams |
| **Structured Output** | Can output JSON for automations |

## Built-in SmartPrompts

Triplo AI comes with a library of pre-built SmartPrompts for common tasks.

### Common Built-in Categories

**Content Creation**:
- Blog Post Generator
- Social Media Post Creator
- Email Drafter
- Article Summarizer
- Content Rewriter

**Analysis**:
- Text Analyzer
- Sentiment Analysis
- Key Points Extractor
- Comparison Tool
- Fact Checker

**Productivity**:
- Meeting Notes Taker
- Task Extractor
- To-Do List Creator
- Priority Sorter
- Action Item Finder

**Technical**:
- Code Explainer
- Code Reviewer
- Documentation Generator
- Bug Finder
- Code Refactorer

**Business**:
- Proposal Drafter
- Report Generator
- Executive Summary
- SWOT Analysis
- Business Plan Outline

### Accessing Built-in SmartPrompts

1. Open Triplo AI
2. Go to SmartPrompts library
3. Browse by category or search
4. Select desired SmartPrompt
5. Provide context (selected text, file, etc.)
6. Execute

## Creating Custom SmartPrompts

### Why Create Custom SmartPrompts?

- **Tailor to your workflow**: Match your specific processes
- **Brand consistency**: Ensure consistent voice and style
- **Domain-specific**: Encode your industry knowledge
- **Team standards**: Share best practices across team
- **Automation-ready**: Output structured data for workflows

### Custom SmartPrompt Structure

A well-designed SmartPrompt includes:

**1. Clear Purpose**
- What does this SmartPrompt do?
- When should it be used?
- What input does it expect?

**2. Role Definition**
- Who is the AI acting as?
- What expertise should it demonstrate?
- What tone should it use?

**3. Task Instructions**
- Step-by-step instructions
- Clear constraints
- Output format requirements

**4. Examples (Optional)**
- Few-shot examples
- Good vs. bad outputs
- Edge cases to handle

**5. Output Specification**
- Format (text, JSON, markdown, etc.)
- Structure (headings, sections, fields)
- Length constraints

### Creating Your First Custom SmartPrompt

**Step 1: Define the Purpose**
- What task do you want to automate?
- What input will you provide?
- What output do you expect?

**Step 2: Write the Prompt**
```
You are a [role]. Your task is to [task].

Input: [describe input]
Process: [step-by-step instructions]
Output: [format and structure]

Constraints:
- [constraint 1]
- [constraint 2]
```

**Step 3: Test and Iterate**
- Test with various inputs
- Check output quality
- Refine instructions
- Add examples if needed

**Step 4: Save as SmartPrompt**
1. Go to SmartPrompts library
2. Click "Create New SmartPrompt"
3. Name your SmartPrompt
4. Paste your prompt
5. Add description and tags
6. Save

### Example Custom SmartPrompt

**Name**: Support Ticket to FAQ Entry

**Prompt**:
```
You are a technical documentation specialist. Convert a customer support ticket into a clear FAQ entry.

Input: A support ticket with customer question and support response.

Process:
1. Identify the core question
2. Extract the solution from the response
3. Rewrite in clear, jargon-free language
4. Add relevant context if helpful
5. Include troubleshooting steps if applicable

Output format:
## [Question]

[Answer in 2-3 paragraphs]

**Troubleshooting**:
- [Step 1]
- [Step 2]

**Related Topics**: [comma-separated tags]

Constraints:
- Keep answer under 200 words
- Use simple language
- Avoid internal jargon
- Focus on actionable steps
```

## Advanced SmartPrompt Techniques

### 1. Structured Output (JSON)

For automations, design SmartPrompts to output structured JSON:

```
You are a content analyst. Extract structured information from the input.

Output valid JSON with this structure:
{
  "title": "string",
  "summary": "string (max 150 chars)",
  "category": "string",
  "tags": ["string"],
  "priority": "number (1-5)",
  "action_items": ["string"],
  "estimated_time": "string"
}
```

**Use with**: Automations, webhooks, API integrations

### 2. Chain-of-Thought Prompting

Guide the AI through reasoning:

```
You are a [role]. Think step-by-step.

Input: [describe input]

Thinking process:
1. First, analyze...
2. Then, consider...
3. Finally, conclude...

Output: [final answer]
```

**Use for**: Complex analysis, debugging, problem-solving

### 3. Few-Shot Learning

Provide examples to guide behavior:

```
You are a [role]. Follow these examples:

Example 1:
Input: [example input]
Output: [example output]

Example 2:
Input: [example input]
Output: [example output]

Now process:
Input: [actual input]
Output:
```

**Use for**: Consistent formatting, style matching

### 4. Conditional Logic

Handle different scenarios:

```
You are a [role]. Process the input according to these rules:

If [condition A]:
  - Do X
  - Output format Y

If [condition B]:
  - Do Z
  - Output format W

Otherwise:
  - Do default action
  - Output default format
```

**Use for**: Multi-scenario workflows

### 5. Role-Based Prompting

Define expertise and perspective:

```
You are a senior [role] with 15 years of experience.

Expertise:
- [area 1]
- [area 2]
- [area 3]

Tone: [professional, friendly, authoritative, etc.]
Perspective: [strategic, tactical, analytical, etc.]

Task: [describe task]
```

**Use for**: Domain-specific tasks, expert analysis

## SmartPrompt Best Practices

### Design Principles

1. **Be Specific**
   - Clear instructions
   - Defined constraints
   - Explicit output format

2. **Be Concise**
   - Remove unnecessary words
   - Focus on essential instructions
   - Avoid ambiguity

3. **Be Consistent**
   - Use similar structure for related prompts
   - Maintain consistent terminology
   - Follow naming conventions

4. **Be Testable**
   - Test with various inputs
   - Verify output quality
   - Handle edge cases

5. **Be Documented**
   - Add clear descriptions
   - Include usage examples
   - Tag for easy discovery

### Common Pitfalls to Avoid

❌ **Too vague**: "Make this better"
✅ **Specific**: "Rewrite this to be more concise and professional"

❌ **Too long**: Pages of instructions
✅ **Focused**: Essential instructions only

❌ **No constraints**: AI can go off-track
✅ **Clear boundaries**: Length, format, tone constraints

❌ **No examples**: AI may misunderstand
✅ **Few-shot examples**: Show desired output

❌ **Inconsistent**: Different structures each time
✅ **Standardized**: Follow template structure

## Organizing SmartPrompts

### Naming Conventions

Use clear, descriptive names:
- `Support Ticket to FAQ Entry`
- `Blog Post Generator - Technical`
- `Meeting Notes to Action Items`
- `Code Review - Security Focus`

### Tagging System

Create tags for:
- **Category**: content, analysis, productivity, technical, business
- **Domain**: marketing, sales, engineering, support
- **Output format**: text, json, markdown, email
- **Complexity**: simple, intermediate, advanced

### Folder Organization

Group related SmartPrompts:
- Content Creation/
- Analysis/
- Productivity/
- Technical/
- Business/

## Sharing SmartPrompts

### Within Your Team

1. Export SmartPrompt
2. Share file or copy-paste
3. Team member imports
4. Test and adapt as needed

### Public Sharing

If Triplo supports community SmartPrompts:
1. Export your SmartPrompt
2. Add description and tags
3. Upload to community library
4. Get feedback and iterate

## SmartPrompt Templates

### Template 1: Content Generator

```
You are a [role]. Generate [content type] about [topic].

Input: [describe input]
Audience: [who is this for?]
Tone: [professional, casual, etc.]
Length: [word count or paragraphs]

Structure:
1. [Section 1]
2. [Section 2]
3. [Section 3]

Output format: [markdown, HTML, etc.]
```

### Template 2: Analyzer

```
You are a [role]. Analyze the input for [purpose].

Input: [describe input]
Analysis focus: [what to look for]
Output format: [structured or narrative]

Key aspects to analyze:
- [aspect 1]
- [aspect 2]
- [aspect 3]

Provide:
1. Summary
2. Key findings
3. Recommendations
```

### Template 3: Converter

```
You are a [role]. Convert [input format] to [output format].

Input: [describe input]
Conversion rules:
- [rule 1]
- [rule 2]
- [rule 3]

Output format: [specify exactly]

Constraints:
- [constraint 1]
- [constraint 2]
```

## Next Steps

- **Learn about Context Awareness**: [`context-awareness-and-sources.md`](context-awareness-and-sources.md)
- **Explore Training/Knowledge Bases**: [`training-and-knowledge-bases.md`](training-and-knowledge-bases.md)
- **Understand Automations**: [`automations-webhooks-api-magnets.md`](automations-webhooks-api-magnets.md)

---

**Official Documentation**: [documentation.triplo.ai/using-triplo-ai/smartprompts](https://documentation.triplo.ai/using-triplo-ai/smartprompts)
