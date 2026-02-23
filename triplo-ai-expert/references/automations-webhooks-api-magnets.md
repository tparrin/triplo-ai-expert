# Automations, Webhooks, API, and Magnets

## What are Triplo Automations?

Triplo Automations allow you to send **structured JSON output** from Triplo AI to external tools via HTTP webhooks and APIs. This turns on-screen content into automated workflows across hundreds of applications.

### Key Concepts

| Concept | What It Does | Why It Matters |
|----------|---------------|----------------|
| **Automation** | Sends AI-generated JSON to external endpoints | Connects Triplo to any webhook-compatible tool |
| **Webhook** | HTTP endpoint that receives data | Standard way to trigger external workflows |
| **API Call** | Makes HTTP requests to external services | Can pull data or push data to APIs |
| **Magnet** | Snaps together models, instructions, Minds, automations | Reusable automation components |

### Why Automations Matter

- **End-to-end workflows**: From on-screen content to multi-app automation
- **Structured output**: JSON format perfect for downstream processing
- **No integrations needed**: Triplo works system-wide, automation handles connections
- **Scalable**: One automation can handle infinite content
- **Flexible**: Works with Zapier, Make, n8n, Activepieces, and more

## How Triplo Automations Work

### The Workflow

```
1. On-screen content (email, ticket, document, etc.)
       ↓
2. Triplo AI processes with SmartPrompt
       ↓
3. AI generates structured JSON output
       ↓
4. Automation maps JSON to webhook parameters
       ↓
5. Webhook sends JSON to external tool
       ↓
6. External tool executes workflow (CRM, CMS, database, etc.)
```

### Example: Support Tickets → Blog Posts

**Step 1: Define Automation in Triplo**
- Function Name: "Ticket to Blog Post"
- Function Description: "Convert support ticket into blog post"
- Parameters: `title`, `summary`, `body`, `category`, `tags`

**Step 2: Configure SmartPrompt**
```
You are a content writer. Convert this support ticket into a blog post.

Output valid JSON:
{
  "title": "string",
  "summary": "string (max 150 chars)",
  "body": "markdown string",
  "category": "string",
  "tags": ["string"]
}
```

**Step 3: Configure Webhook**
- Webhook URL: `https://your-automation-tool.com/webhook`
- HTTP Method: POST
- Headers: `{"Authorization": "Bearer YOUR_KEY"}`
- Payload: Auto-generated from parameters

**Step 4: Execute**
1. Select support ticket
2. Trigger Triplo
3. Type "Ticket to Blog Post" or use hotkey
4. Triplo generates JSON
5. Automation sends to webhook
6. External tool creates blog post in CMS

## Creating an Automation

### Step 1: Define Function

**Function Name**: The trigger phrase you'll use
- Example: "Ticket to Blog Post"
- Example: "Lead to CRM"
- Example: "Meeting Notes to Tasks"

**Function Description**: What the automation does
- Clear description of purpose
- Helps Triplo understand context
- Useful for documentation

### Step 2: Define Parameters

Parameters define what data the automation will send:

```json
{
  "title": "Blog post title",
  "summary": "Brief summary",
  "body": "Full blog post content",
  "category": "Content category",
  "tags": ["tag1", "tag2"]
}
```

**Best practices**:
- Use descriptive parameter names
- Define data types (string, number, array)
- Include constraints (max length, required fields)
- Match downstream tool's expected format

### Step 3: Configure Webhook

**Webhook URL**: The endpoint that will receive data
- From your automation tool (Zapier, Make, Activepieces, etc.)
- Must be HTTPS for security
- Test URL before using

**HTTP Method**: How to send data
- **POST**: Most common for webhooks
- **PUT**: For updating existing data
- **GET**: For pulling data (API calls)

**Headers**: Authentication and metadata
```json
{
  "Content-Type": "application/json",
  "Authorization": "Bearer YOUR_API_KEY"
}
```

**Payload**: The JSON structure to send
- Triplo can auto-suggest based on parameters
- Edit as needed
- Test before using

### Step 4: Configure SmartPrompt

The SmartPrompt generates the JSON that matches your parameters:

```
You are a [role]. Process the input and output structured JSON.

Input: [describe input context]

Output valid JSON with this structure:
{
  "param1": "description",
  "param2": "description",
  "param3": ["array", "items"]
}

Constraints:
- [constraint 1]
- [constraint 2]
```

**Key points**:
- Output must be valid JSON
- Must match your parameter structure
- Include constraints for quality
- Test with sample inputs

### Step 5: Test and Deploy

**Testing workflow**:
1. Test SmartPrompt with sample input
2. Verify JSON output is valid
3. Test webhook with sample payload
4. Verify external tool receives data
5. Run full end-to-end test

**Deployment**:
1. Enable automation in Triplo settings
2. Configure user confirmation (optional)
3. Set up hotkey if desired
4. Document automation for team

## Magnets: Reusable Automation Components

### What are Magnets?

Magnets "snap together" different components to create reusable automation patterns:

**Magnet Components**:
- **Model**: Which AI model to use
- **Instructions**: The prompt or SmartPrompt
- **Mind**: Which knowledge base to reference
- **Automation**: The webhook/API configuration

### Creating Magnets

**Example Magnet: Content Publisher**

**Components**:
- Model: GPT-4 (for high-quality output)
- Instructions: "Convert to blog post" SmartPrompt
- Mind: Company Style Guide
- Automation: CMS webhook

**Usage**:
- Select any content
- Trigger "Content Publisher" Magnet
- Get consistent, branded blog post
- Automatically published to CMS

**Benefits**:
- Consistent output quality
- Reusable across content types
- Combines multiple settings
- One-click execution

## Automation Scenarios

### Scenario 1: Support Tickets → Knowledge Base

**Workflow**:
1. Support agent selects ticket in help desk
2. Trigger Triplo with "Ticket to KB" automation
3. Triplo extracts solution and creates FAQ entry
4. Automation sends JSON to knowledge base tool
5. KB tool creates new FAQ article
6. Team reviews and publishes

**JSON Structure**:
```json
{
  "question": "Customer's question",
  "answer": "Solution from response",
  "category": "Product category",
  "tags": ["relevant", "tags"],
  "priority": "high/medium/low"
}
```

**Tools**: Notion, Confluence, Guru, Help Scout

### Scenario 2: Sales Calls → CRM Entry

**Workflow**:
1. Sales rep selects call transcript
2. Trigger Triplo with "Call to CRM" automation
3. Triplo extracts lead info and action items
4. Automation sends JSON to CRM webhook
5. CRM creates/updates lead record
6. Tasks assigned to appropriate team

**JSON Structure**:
```json
{
  "company": "Company name",
  "contact": "Contact name",
  "email": "contact@email.com",
  "phone": "phone number",
  "stage": "deal stage",
  "action_items": ["item1", "item2"],
  "next_steps": "next action"
}
```

**Tools**: HubSpot, Salesforce, Pipedrive, Close

### Scenario 3: Research Notes → Report

**Workflow**:
1. Researcher selects notes from multiple sources
2. Trigger Triplo with "Notes to Report" automation
3. Triplo synthesizes into structured report
4. Automation sends JSON to report generator
5. Report tool creates formatted document
6. Team reviews and edits

**JSON Structure**:
```json
{
  "title": "Report title",
  "executive_summary": "brief summary",
  "findings": [
    {
      "topic": "finding topic",
      "details": "finding details",
      "source": "source reference"
    }
  ],
  "recommendations": ["rec1", "rec2"]
}
```

**Tools**: Google Docs, Notion, Confluence, Microsoft Word

### Scenario 4: Social Media → Content Calendar

**Workflow**:
1. Marketer selects trending topic or content
2. Trigger Triplo with "Topic to Social" automation
3. Triplo generates social posts for multiple platforms
4. Automation sends JSON to social media tool
5. Social tool schedules posts across platforms
6. Analytics tracked automatically

**JSON Structure**:
```json
{
  "campaign": "campaign name",
  "posts": [
    {
      "platform": "Twitter",
      "content": "post content",
      "hashtags": ["#tag1", "#tag2"],
      "schedule": "date/time"
    }
  ]
}
```

**Tools**: Buffer, Hootsuite, Sprout Social

## Integration with Automation Tools

### Activepieces

**Why Activepieces**:
- 635+ connectors (Google Sheets, Notion, CRMs, etc.)
- AI steps and agents within workflows
- Central datastore for structured data
- Webhook triggers supported

**Integration pattern**:
1. Create flow in Activepieces with webhook trigger
2. Copy webhook URL
3. Paste into Triplo automation
4. Triplo sends JSON to Activepieces
5. Activepieces executes workflow across multiple tools

**Example flow**:
```
Webhook (from Triplo)
  → Parse JSON
  → Add row to Google Sheets
  → Create record in HubSpot
  → Send email via Gmail
  → Post to Slack channel
```

### Zapier

**Why Zapier**:
- Huge app ecosystem (5000+ apps)
- Simple to set up
- Reliable and well-supported
- Webhooks by Zapier feature

**Integration pattern**:
1. Create Zap with "Webhooks by Zapier" trigger
2. Copy webhook URL
3. Paste into Triplo automation
4. Triplo sends JSON to Zapier
5. Zapier executes action in connected apps

### Make (Integromat)

**Why Make**:
- Extremely flexible visual builder
- Complex branching and data transformation
- Strong API support
- Good for advanced workflows

**Integration pattern**:
1. Create scenario with Webhook module
2. Copy webhook URL
3. Paste into Triplo automation
4. Triplo sends JSON to Make
5. Make processes through complex workflow

### n8n

**Why n8n**:
- Open-source and self-hostable
- Strong native AI support
- Excellent for technical users
- Custom nodes and integrations

**Integration pattern**:
1. Create workflow with Webhook node
2. Copy webhook URL
3. Paste into Triplo automation
4. Triplo sends JSON to n8n
5. n8n executes workflow with AI steps

## Best Practices

### For Automation Design

1. **Start simple**
   - Begin with basic JSON structure
   - Test thoroughly
   - Add complexity gradually

2. **Validate JSON**
   - Ensure output is valid JSON
   - Test with sample inputs
   - Use JSON validators

3. **Handle errors**
   - What if webhook fails?
   - What if JSON is invalid?
   - What if external tool is down?

4. **Document everything**
   - Automation purpose
   - JSON structure
   - Webhook endpoint
   - Dependencies

### For SmartPrompt Design

1. **Be specific about output format**
   - Define exact JSON structure
   - Specify data types
   - Include constraints

2. **Provide examples**
   - Show desired output
   - Include edge cases
   - Demonstrate format

3. **Test extensively**
   - Test with various inputs
   - Verify JSON validity
   - Check quality of output

### For Workflow Design

1. **Map end-to-end flow**
   - From content to final action
   - Identify all steps
   - Note dependencies

2. **Choose right tools**
   - Match tool to task
   - Consider cost and complexity
   - Evaluate reliability

3. **Monitor and iterate**
   - Track success rates
   - Gather feedback
   - Improve over time

## Constraints and Limitations

### Important Constraints

**Automations are desktop-only**:
- Not available on mobile
- Requires desktop Triplo AI

**Relies on OpenAI models**:
- Cannot use OpenRouter models for automations
- Must use OpenAI-compatible models

**Sends JSON only**:
- Output must be valid JSON
- Cannot send other formats

**User confirmation by default**:
- Triplo asks for confirmation before sending
- Can be disabled in settings

### Workarounds

**Mobile workaround**:
- Use desktop for automation setup
- Mobile for content selection
- Sync via cloud or clipboard

**Model workaround**:
- Use OpenAI models for automation
- Use OpenRouter for other tasks

**Format workaround**:
- Convert non-JSON to JSON in SmartPrompt
- Use automation tool for formatting

## Troubleshooting

### Common Issues

**Issue: Webhook not receiving data**
- **Solution**: Verify URL is correct, test with sample payload
- **Check**: Webhook is active and accessible

**Issue: JSON is invalid**
- **Solution**: Test SmartPrompt output, validate JSON
- **Check**: Parameter names match structure

**Issue: External tool not processing**
- **Solution**: Verify tool can handle JSON, check authentication
- **Check**: Tool's webhook configuration

**Issue: Automation not triggering**
- **Solution**: Ensure automation is enabled, check hotkey
- **Verify**: Function name matches trigger

## Next Steps

- **Learn about Agents**: [`agents-and-connections.md`](agents-and-connections.md)
- **Explore Models**: [`models-allowances-and-byok.md`](models-allowances-and-byok.md)
- **Understand Local Models**: [`local-llms-setup-desktop-mobile.md`](local-llms-setup-desktop-mobile.md)

---

**Official Documentation**: [documentation.triplo.ai/using-triplo-ai/automations](https://documentation.triplo.ai/using-triplo-ai/automations)
