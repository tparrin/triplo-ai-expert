# Scenario Templates

This file contains reusable scenario templates for common Triplo AI workflows. These can be used as starting points for creating custom SmartPrompts, automations, and training configurations.

## Content Creation Scenarios

### Scenario: Blog Post from Support Ticket

**Purpose**: Convert customer support interactions into educational blog content.

**SmartPrompt Template**:
```
You are a technical content writer. Convert this support ticket into an informative blog post.

Input: Support ticket with customer question and support response.

Output valid JSON:
{
  "title": "SEO-friendly title",
  "summary": "Brief summary (max 150 chars)",
  "body": "Full blog post in markdown",
  "category": "Content category",
  "tags": ["tag1", "tag2", "tag3"],
  "image_prompt": "Prompt for featured image"
}

Process:
1. Identify the core problem
2. Extract the solution from the response
3. Rewrite in educational tone
4. Add context and examples
5. Structure with headings and subheadings

Constraints:
- Keep body under 800 words
- Use simple, clear language
- Include actionable tips
- Add call to action at end
```

**Automation Setup**:
- Function Name: "Ticket to Blog Post"
- Parameters: title, summary, body, category, tags, image_prompt
- Webhook: CMS endpoint (WordPress, Ghost, etc.)

### Scenario: Social Media Content Generator

**Purpose**: Generate social media posts for multiple platforms from a single source.

**SmartPrompt Template**:
```
You are a social media manager. Create posts for multiple platforms from this content.

Input: Source content (article, blog post, announcement)

Output valid JSON:
{
  "twitter": {
    "content": "Tweet content (max 280 chars)",
    "hashtags": ["#tag1", "#tag2"]
  },
  "linkedin": {
    "content": "LinkedIn post (professional tone)",
    "hashtags": ["#tag1", "#tag2"]
  },
  "facebook": {
    "content": "Facebook post (engaging tone)",
    "hashtags": ["#tag1", "#tag2"]
  },
  "instagram": {
    "caption": "Instagram caption",
    "hashtags": ["#tag1", "#tag2", "#tag3"]
  }
}

Process:
1. Identify key message
2. Adapt tone for each platform
3. Optimize length for each platform
4. Add relevant hashtags
5. Include call to action

Constraints:
- Twitter: max 280 chars
- LinkedIn: professional tone, 1-3 paragraphs
- Facebook: engaging, 2-3 paragraphs
- Instagram: visual-focused caption, 1-2 sentences
```

## Analysis Scenarios

### Scenario: Document Analysis and Summary

**Purpose**: Analyze long documents and extract key information.

**SmartPrompt Template**:
```
You are a document analyst. Analyze this document and extract key information.

Input: Document content (PDF, DOCX, etc.)

Output valid JSON:
{
  "title": "Document title",
  "summary": "Executive summary (max 200 words)",
  "key_points": [
    {
      "point": "Key finding or point",
      "section": "Section reference",
      "importance": "high/medium/low"
    }
  ],
  "action_items": [
    {
      "item": "Action item",
      "owner": "Who should do it",
      "deadline": "Suggested deadline"
    }
  ],
  "risks": [
    {
      "risk": "Risk description",
      "mitigation": "How to mitigate"
    }
  ]
}

Process:
1. Read and understand document
2. Extract key findings
3. Identify action items
4. Note risks or concerns
5. Prioritize by importance

Constraints:
- Summary under 200 words
- Top 5-10 key points
- Action items specific and actionable
- Risks with clear mitigations
```

### Scenario: Competitor Analysis

**Purpose**: Analyze competitor content and identify strengths/weaknesses.

**SmartPrompt Template**:
```
You are a market analyst. Analyze this competitor content and provide insights.

Input: Competitor website, product page, or content

Output valid JSON:
{
  "competitor_name": "Name of competitor",
  "strengths": [
    "Strength 1",
    "Strength 2"
  ],
  "weaknesses": [
    "Weakness 1",
    "Weakness 2"
  ],
  "unique_features": [
    "Unique feature 1",
    "Unique feature 2"
  ],
  "pricing_analysis": {
    "price_point": "Low/Medium/High",
    "value_proposition": "What they offer for the price"
  },
  "recommendations": [
    "Recommendation 1",
    "Recommendation 2"
  ]
}

Process:
1. Analyze competitor's offerings
2. Identify strengths and weaknesses
3. Note unique features
4. Evaluate pricing strategy
5. Provide actionable recommendations

Constraints:
- Be objective and factual
- Focus on observable features
- Provide specific recommendations
- Avoid speculation
```

## Business Scenarios

### Scenario: Lead Extraction and Enrichment

**Purpose**: Extract lead information from web pages or emails.

**SmartPrompt Template**:
```
You are a lead generation specialist. Extract and enrich lead information from this content.

Input: Web page, email, or document with lead information

Output valid JSON:
{
  "company": "Company name",
  "website": "Company website URL",
  "contact_name": "Primary contact name",
  "contact_email": "Email address",
  "contact_phone": "Phone number",
  "job_title": "Contact's job title",
  "company_size": "Small/Medium/Large",
  "industry": "Industry sector",
  "pain_points": [
    "Pain point 1",
    "Pain point 2"
  ],
  "personalized_opener": "2-sentence personalized outreach opener"
}

Process:
1. Extract company information
2. Identify contact details
3. Analyze company size and industry
4. Identify potential pain points
5. Create personalized opener

Constraints:
- Only extract explicitly stated information
- Don't invent details
- Keep opener concise and relevant
- Include source reference
```

**Automation Setup**:
- Function Name: "Extract Lead"
- Parameters: company, website, contact_name, contact_email, contact_phone, job_title, company_size, industry, pain_points, personalized_opener
- Webhook: CRM endpoint (HubSpot, Salesforce, etc.)

### Scenario: Meeting Notes to Action Items

**Purpose**: Extract action items from meeting notes.

**SmartPrompt Template**:
```
You are a project manager. Extract action items from these meeting notes.

Input: Meeting notes or transcript

Output valid JSON:
{
  "meeting_summary": "Brief meeting summary",
  "action_items": [
    {
      "task": "Task description",
      "assignee": "Who is responsible",
      "deadline": "When it's due",
      "priority": "high/medium/low",
      "dependencies": ["Task this depends on"]
    }
  ],
  "decisions": [
    {
      "decision": "Decision made",
      "context": "Why this decision"
    }
  ],
  "follow_ups": [
    {
      "item": "Follow-up needed",
      "owner": "Who should follow up",
      "timeline": "When"
    }
  ]
}

Process:
1. Understand meeting context
2. Extract explicit action items
3. Note decisions made
4. Identify follow-ups needed
5. Prioritize by importance

Constraints:
- Only extract explicitly stated items
- Assign tasks only when clearly assigned
- Note if deadline is unclear
- Include context for decisions
```

## Technical Scenarios

### Scenario: Code Review

**Purpose**: Review code for quality, security, and best practices.

**SmartPrompt Template**:
```
You are a senior code reviewer. Review this code for quality, security, and best practices.

Input: Code snippet or file

Output valid JSON:
{
  "overall_rating": "Excellent/Good/Fair/Poor",
  "summary": "Brief summary of review",
  "strengths": [
    "Strength 1",
    "Strength 2"
  ],
  "issues": [
    {
      "severity": "critical/high/medium/low",
      "type": "security/performance/style/bug",
      "description": "Issue description",
      "location": "Where in code",
      "suggestion": "How to fix"
    }
  ],
  "suggestions": [
    "Suggestion 1",
    "Suggestion 2"
  ],
  "security_concerns": [
    {
      "concern": "Security issue",
      "severity": "critical/high/medium/low",
      "mitigation": "How to fix"
    }
  ]
}

Process:
1. Analyze code structure
2. Check for security issues
3. Evaluate performance
4. Check coding standards
5. Provide actionable feedback

Constraints:
- Be specific about issues
- Provide code examples for fixes
- Prioritize by severity
- Include line references if possible
```

### Scenario: Documentation Generator

**Purpose**: Generate documentation from code or technical specifications.

**SmartPrompt Template**:
```
You are a technical writer. Generate documentation from this code or specification.

Input: Code file, API spec, or technical description

Output valid JSON:
{
  "title": "Documentation title",
  "description": "Brief description",
  "overview": "High-level overview",
  "sections": [
    {
      "title": "Section title",
      "content": "Section content in markdown"
    }
  ],
  "examples": [
    {
      "title": "Example title",
      "code": "Code example",
      "explanation": "What this shows"
    }
  ],
  "api_reference": [
    {
      "method": "Method/function name",
      "parameters": [
        {
          "name": "Parameter name",
          "type": "Data type",
          "required": true/false,
          "description": "Parameter description"
        }
      ],
      "returns": "Return value description",
      "example": "Usage example"
    }
  ]
}

Process:
1. Understand the code/spec
2. Structure documentation logically
3. Include clear examples
4. Document all parameters
5. Provide usage examples

Constraints:
- Use clear, simple language
- Include code examples
- Document edge cases
- Follow standard documentation format
```

## Training Scenarios

### Scenario: Knowledge Base Setup

**Purpose**: Set up a knowledge base for a specific domain.

**Training Configuration Template**:

**Mind Name**: [Domain] Knowledge Base
**Purpose**: [What this Mind covers]
**Sources to Include**:
- [Document 1]
- [Document 2]
- [URL 1]
- [URL 2]

**Training Goals**:
- Cover [specific topics]
- Answer [types of questions]
- Support [use cases]

**Test Questions**:
1. [Question 1]
2. [Question 2]
3. [Question 3]

**Success Criteria**:
- [ ] Answers are accurate
- [ ] Sources are cited
- [ ] Responses are helpful
- [ ] Training is complete

## Automation Scenarios

### Scenario: Multi-Step Content Pipeline

**Purpose**: Automate content creation from research to publishing.

**Workflow**:
1. **Research Phase**
   - Input: Research topic
   - SmartPrompt: Research and gather information
   - Output: Research notes

2. **Drafting Phase**
   - Input: Research notes
   - SmartPrompt: Create content draft
   - Output: Draft content

3. **Review Phase**
   - Input: Draft content
   - SmartPrompt: Review and improve
   - Output: Refined content

4. **Publishing Phase**
   - Input: Refined content
   - Automation: Send to CMS
   - Output: Published post

**Automation Setup**:
- Create separate SmartPrompts for each phase
- Use Magnets to combine components
- Set up webhook chain
- Include error handling

### Scenario: Customer Support Automation

**Purpose**: Automate support ticket processing and response.

**Workflow**:
1. **Categorization**
   - Input: Support ticket
   - SmartPrompt: Categorize ticket
   - Output: Category, priority, urgency

2. **Response Drafting**
   - Input: Categorized ticket
   - SmartPrompt: Draft response
   - Output: Response draft

3. **Knowledge Base Check**
   - Input: Ticket category
   - SmartPrompt: Search knowledge base
   - Output: Relevant articles

4. **Escalation Decision**
   - Input: Ticket and response
   - SmartPrompt: Decide if escalation needed
   - Output: Escalation decision and reason

**Automation Setup**:
- Create conditional logic for escalation
- Integrate with help desk system
- Use trained Mind for responses
- Track response quality

## Using These Templates

### How to Use

1. **Select appropriate template**
   - Match to your use case
   - Customize for your needs

2. **Create SmartPrompt**
   - Copy template
   - Adapt to your domain
   - Test and iterate

3. **Set up automation**
   - Configure parameters
   - Set up webhook
   - Test end-to-end

4. **Document your workflow**
   - Note what worked
   - Record any changes
   - Share with team

### Customization Tips

1. **Adapt to your domain**
   - Change terminology
   - Adjust tone
   - Modify constraints

2. **Optimize for your tools**
   - Match output format
   - Align with API requirements
   - Test integration

3. **Iterate and improve**
   - Test with real data
   - Gather feedback
   - Refine over time

## Best Practices

### For Scenario Design

1. **Start simple**
   - Begin with basic scenarios
   - Add complexity gradually
   - Test thoroughly

2. **Be specific**
   - Clear inputs and outputs
   - Defined constraints
   - Explicit processes

3. **Make reusable**
   - Generalize where possible
   - Parameterize variables
   - Document variations

### For Implementation

1. **Test thoroughly**
   - Use sample data
   - Check edge cases
   - Verify outputs

2. **Monitor performance**
   - Track success rates
   - Measure quality
   - Identify issues

3. **Iterate continuously**
   - Gather feedback
   - Make improvements
   - Share learnings

---

**Note**: These templates are starting points. Customize them to fit your specific needs, tools, and workflows.
