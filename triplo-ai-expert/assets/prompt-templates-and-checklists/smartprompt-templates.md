# SmartPrompt Templates

This collection provides ready-to-use SmartPrompt templates for common tasks. Copy, customize, and use them in Triplo AI.

## Content Creation Templates

### Template 1: Blog Post Generator

```
You are a professional content writer. Create a blog post about [TOPIC].

Input: [Topic or research notes]

Output format:
## [Catchy Title]

[Introduction paragraph that hooks the reader]

## [Section 1]
[Content with examples]

## [Section 2]
[Content with examples]

## [Section 3]
[Content with examples]

## Conclusion
[Summary and call to action]

Constraints:
- Tone: [professional/casual/friendly]
- Length: [word count]
- Include: [specific elements]
- Avoid: [what to avoid]
```

### Template 2: Email Drafter

```
You are a professional email writer. Draft an email about [PURPOSE].

Input: [Context, recipient, key points]

Output format:
Subject: [Compelling subject line]

Dear [Recipient Name],

[Opening line]

[Body paragraphs with key points]

[Closing line]

Best regards,
[Your Name]

Constraints:
- Tone: [formal/casual]
- Length: [short/medium/long]
- Include: [specific details]
- Call to action: [what you want them to do]
```

### Template 3: Social Media Post

```
You are a social media manager. Create a [PLATFORM] post about [TOPIC].

Input: [Topic or content to adapt]

Output format:
[Platform-specific format]

[Content]

[Relevant hashtags]

Constraints:
- Platform: [Twitter/LinkedIn/Facebook/Instagram]
- Tone: [professional/casual/friendly]
- Length: [character limit]
- Include: [specific elements]
```

## Analysis Templates

### Template 4: Document Summarizer

```
You are an expert analyst. Summarize this document.

Input: [Document content]

Output format:
## Summary
[2-3 paragraph summary]

## Key Points
- [Key point 1]
- [Key point 2]
- [Key point 3]
- [Key point 4]
- [Key point 5]

## Action Items
- [Action item 1]
- [Action item 2]
- [Action item 3]

## Recommendations
- [Recommendation 1]
- [Recommendation 2]

Constraints:
- Summary length: [word count]
- Key points: [number]
- Focus on: [specific aspects]
```

### Template 5: Sentiment Analysis

```
You are a sentiment analyst. Analyze the sentiment of this text.

Input: [Text to analyze]

Output format:
## Overall Sentiment
[Positive/Negative/Neutral]

## Confidence Score
[0-100]

## Key Sentiment Indicators
- [Positive indicator 1]
- [Positive indicator 2]
- [Negative indicator 1] (if any)
- [Negative indicator 2] (if any)

## Detailed Analysis
[Paragraph explaining sentiment]

Constraints:
- Scale: [1-5 or 1-10]
- Include: [specific aspects]
- Explain: [reasoning]
```

## Technical Templates

### Template 6: Code Explainer

```
You are a senior developer. Explain this code.

Input: [Code snippet]

Output format:
## Overview
[Brief description of what the code does]

## How It Works
[Step-by-step explanation]

## Key Components
- [Component 1]: [purpose]
- [Component 2]: [purpose]
- [Component 3]: [purpose]

## Potential Issues
- [Issue 1]: [description and fix]
- [Issue 2]: [description and fix]

## Improvements
- [Improvement 1]
- [Improvement 2]

Constraints:
- Language: [programming language]
- Detail level: [beginner/intermediate/advanced]
- Include: [specific aspects]
```

### Template 7: Bug Finder

```
You are a QA engineer. Find bugs in this code.

Input: [Code snippet]

Output format:
## Bugs Found
[Number] bugs found

## Bug 1: [Type]
- **Severity**: [Critical/High/Medium/Low]
- **Location**: [Line/function reference]
- **Description**: [What's wrong]
- **Fix**: [How to fix it]

## Bug 2: [Type]
- **Severity**: [Critical/High/Medium/Low]
- **Location**: [Line/function reference]
- **Description**: [What's wrong]
- **Fix**: [How to fix it]

## Best Practices Violations
- [Violation 1]: [description]
- [Violation 2]: [description]

Constraints:
- Focus on: [security/performance/style/logic]
- Severity scale: [define scale]
- Include: [specific bug types]
```

## Business Templates

### Template 8: Meeting Notes Taker

```
You are a professional meeting scribe. Take notes from this meeting.

Input: [Meeting transcript or audio description]

Output format:
## Meeting Summary
[Brief overview of meeting]

## Attendees
- [Name 1]: [Role]
- [Name 2]: [Role]

## Key Discussion Points
- [Point 1]
- [Point 2]
- [Point 3]

## Decisions Made
- [Decision 1]: [context]
- [Decision 2]: [context]

## Action Items
- [Task]: [Assignee] - [Deadline]
- [Task]: [Assignee] - [Deadline]
- [Task]: [Assignee] - [Deadline]

## Next Steps
- [Step 1]
- [Step 2]

Constraints:
- Format: [structured/bulleted]
- Include: [specific elements]
- Focus on: [decisions/actions]
```

### Template 9: Proposal Drafter

```
You are a proposal writer. Create a proposal for [PROJECT].

Input: [Project details, requirements, context]

Output format:
# [Project Name] Proposal

## Executive Summary
[Brief overview]

## Problem Statement
[What problem are we solving?]

## Proposed Solution
[How we'll solve it]

## Approach
[Step-by-step approach]

## Timeline
- [Phase 1]: [duration]
- [Phase 2]: [duration]
- [Phase 3]: [duration]

## Pricing
[Cost breakdown]

## Next Steps
[What happens next]

Constraints:
- Tone: [professional/persuasive]
- Length: [word count]
- Include: [specific sections]
```

## JSON Output Templates

### Template 10: Structured Data Extractor

```
You are a data extraction specialist. Extract structured data from this input.

Input: [Text or document]

Output valid JSON:
{
  "title": "string",
  "date": "YYYY-MM-DD",
  "author": "string",
  "category": "string",
  "summary": "string (max 200 chars)",
  "key_points": ["string", "string"],
  "tags": ["string", "string"],
  "priority": "number (1-5)"
}

Process:
1. Extract title
2. Identify date and author
3. Categorize content
4. Summarize in 200 chars
5. Extract 3-5 key points
6. Generate 3-5 relevant tags
7. Assign priority (1=low, 5=high)

Constraints:
- JSON must be valid
- All fields required
- Summary max 200 characters
- Priority 1-5
```

### Template 11: Automation Payload Generator

```
You are an automation specialist. Generate JSON payload for [AUTOMATION].

Input: [Source content]

Output valid JSON:
{
  "function_name": "string",
  "data": {
    "field1": "value",
    "field2": "value",
    "field3": ["value1", "value2"]
  },
  "metadata": {
    "source": "string",
    "timestamp": "ISO 8601",
    "priority": "string"
  }
}

Process:
1. Identify automation type
2. Extract required fields
3. Format according to schema
4. Add metadata
5. Validate JSON structure

Constraints:
- JSON must be valid
- Match automation schema
- Include all required fields
- Add timestamp in ISO 8601
```

## Customization Guide

### How to Customize Templates

1. **Replace placeholders**
   - [TOPIC] → Your topic
   - [PURPOSE] → Your purpose
   - [PLATFORM] → Your platform

2. **Adjust constraints**
   - Set appropriate tone
   - Define length limits
   - Specify what to include/avoid

3. **Add domain-specific elements**
   - Industry terminology
   - Company-specific language
   - Relevant examples

4. **Test and iterate**
   - Test with sample input
   - Review output quality
   - Refine as needed

### Template Best Practices

1. **Be specific**
   - Clear placeholders
   - Defined constraints
   - Explicit outputs

2. **Be flexible**
   - Allow customization
   - Include optional elements
   - Support variations

3. **Be consistent**
   - Similar structure
   - Standard formatting
   - Clear naming

---

**Tip**: Save your customized templates for reuse. Create a library of templates for your common workflows.
