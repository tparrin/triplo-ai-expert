# Training and Knowledge Bases

## What are Training, Minds, and Knowledge Bases?

Triplo AI's Training feature lets you build **trusted knowledge bases** from your documents, URLs, and other sources. These knowledge bases (called "Minds") ensure AI responses are grounded in your actual information rather than generic web knowledge.

### Key Concepts

| Concept | What It Is | Why It Matters |
|----------|-------------|----------------|
| **Training** | The process of teaching Triplo your information | Creates domain-specific knowledge |
| **Mind** | A trained knowledge base on a specific topic | Organizes your knowledge by domain |
| **Knowledge Base** | Collection of documents and sources | Provides the raw material for training |

### Benefits of Training

- **Accuracy**: Responses based on your actual data
- **Consistency**: Same information every time
- **Trust**: Know where information comes from
- **Relevance**: Domain-specific, not generic
- **Privacy**: Your data stays with you

## Creating a Mind

### Step 1: Define Your Mind's Purpose

Before training, define what your Mind will cover:

**Questions to ask**:
- What domain will this Mind cover?
- What types of questions should it answer?
- Who will use this Mind?
- What documents do I have?

**Example Minds**:
- **Company Policies**: HR documents, employee handbook
- **Product Documentation**: User manuals, API docs
- **Research Papers**: Academic papers, studies
- **Customer Support**: FAQ, troubleshooting guides
- **Legal Documents**: Contracts, regulations

### Step 2: Gather Your Sources

**Supported Source Types**:

| Source Type | Format | Best For |
|-------------|---------|----------|
| **Documents** | PDF, DOCX, TXT, MD | Formal documents, reports |
| **Webpages** | URLs | Online documentation, articles |
| **Files** | CSV, JSON, XML | Structured data |
| **Code** | Various programming languages | Code documentation, APIs |

**Best practices for gathering**:
- Use recent, accurate documents
- Remove outdated information
- Organize by topic or category
- Ensure consistent formatting

### Step 3: Create and Train Your Mind

**How to create a Mind**:
1. Open Triplo AI
2. Go to Training / Minds section
3. Click "Create New Mind"
4. Name your Mind (descriptive name)
5. Add description and tags
6. Upload or link your sources
7. Click "Train"

**Training process**:
- Triplo processes your documents
- Creates searchable knowledge base
- Indexes content for retrieval
- May take time depending on source size

**Training indicators**:
- Progress bar shows completion
- Status updates during training
- Notification when complete

### Step 4: Test Your Mind

**Testing workflow**:
1. Enable your Mind in settings
2. Ask questions related to your domain
3. Verify answers are accurate
4. Check that sources are cited
5. Refine if needed

**Test questions**:
- "What does our policy say about X?"
- "How do I troubleshoot Y?"
- "What are the key features of product Z?"

## Managing Multiple Minds

### When to Use Multiple Minds

**Use separate Minds when**:
- Domains are distinct (e.g., HR vs. Engineering)
- Different teams need different knowledge
- Information is sensitive and should be segmented
- You want to control which Mind is active

**Example Mind structure**:
- Company Policies (HR)
- Product Documentation (Engineering)
- Sales Materials (Sales)
- Support Knowledge (Customer Service)
- Legal Compliance (Legal)

### Mind Organization

**Naming conventions**:
- Use clear, descriptive names
- Include domain or team
- Example: "HR-Policies-2024", "Product-API-Docs"

**Tagging system**:
- Tag by department (HR, Engineering, Sales)
- Tag by type (Policies, Docs, FAQs)
- Tag by sensitivity (Public, Internal, Confidential)

**Folder structure** (if supported):
- Department/
  - HR/
  - Engineering/
  - Sales/
- Type/
  - Policies/
  - Documentation/
  - FAQs/

### Enabling and Disabling Minds

**How to manage active Minds**:
1. Go to Training / Minds section
2. View all your Minds
3. Toggle Minds on/off
4. Set default Mind (if applicable)
5. Save settings

**Best practices**:
- Only enable relevant Minds for current task
- Disable Minds with conflicting information
- Use default Mind for general queries
- Switch Minds based on context

## Building Effective Knowledge Bases

### Content Quality

**What makes a good knowledge base**:

✅ **Good**:
- Accurate, up-to-date information
- Clear, well-structured documents
- Consistent terminology
- Comprehensive coverage
- Proper formatting

❌ **Bad**:
- Outdated or incorrect information
- Poorly formatted documents
- Inconsistent terminology
- Gaps in coverage
- Duplicate or conflicting content

### Document Preparation

**Before uploading**:
1. **Clean up documents**
   - Remove unnecessary formatting
   - Fix typos and errors
   - Standardize terminology

2. **Organize content**
   - Use clear headings
   - Include table of contents
   - Add metadata (tags, categories)

3. **Remove duplicates**
   - Check for repeated information
   - Consolidate similar content
   - Resolve conflicts

4. **Add context**
   - Include publication dates
   - Note document versions
   - Add author information

### Source Selection

**What to include**:
- Official documentation
- Policies and procedures
- FAQs and troubleshooting guides
- Product specifications
- Best practices and guidelines

**What to exclude**:
- Personal notes (unless relevant)
- Draft or incomplete documents
- Outdated versions
- Confidential information (unless appropriate)

## Using Minds with SmartPrompts

### Combining Training + SmartPrompts

Training and SmartPrompts work together powerfully:

**Workflow**:
1. Train a Mind on your domain
2. Create a SmartPrompt that references the Mind
3. Use the SmartPrompt to query your knowledge base

**Example**:
- **Mind**: Company Policies
- **SmartPrompt**: "Policy Checker"
- **Use**: "Check if this action complies with policy"

### SmartPrompt Templates for Minds

**Template 1: Knowledge Query**
```
You are an expert on [domain]. Use the [Mind Name] knowledge base to answer questions.

Input: [user question]

Process:
1. Search [Mind Name] for relevant information
2. Synthesize findings
3. Provide clear, accurate answer
4. Cite sources from the knowledge base

Output format:
## Answer
[Your answer]

**Sources**:
- [Source 1]
- [Source 2]
```

**Template 2: Document Search**
```
You are a document specialist. Search [Mind Name] for specific information.

Input: [search query]

Process:
1. Find all relevant documents in [Mind Name]
2. Extract key information
3. Summarize findings
4. Provide document references

Output:
**Found in**: [number] documents
**Key Information**: [summary]
**Documents**: [list of documents]
```

## Advanced Training Techniques

### Incremental Training

**Add new sources over time**:
1. Start with core documents
2. Train initial Mind
3. Test and validate
4. Add more sources
5. Retrain Mind
6. Repeat as needed

**Benefits**:
- Faster initial training
- Easier to identify issues
- Gradual improvement
- Less rework needed

### Versioning Minds

**Track changes to your knowledge base**:
1. Create version tags (v1.0, v1.1, etc.)
2. Document what changed
3. Keep old versions if needed
4. Roll back if problems occur

**When to version**:
- Major content updates
- Policy changes
- New product releases
- Restructuring knowledge base

### Cross-Referencing Minds

**Link related information across Minds**:
- Reference other Minds in documents
- Create cross-Mind queries
- Use tags to connect related content

**Example**:
- HR Policies Mind references Employee Handbook
- Product Docs Mind references API Documentation
- Support Mind references both HR and Product Minds

## Best Practices

### For Effective Training

1. **Start small**
   - Begin with core documents
   - Test thoroughly
   - Expand gradually

2. **Keep it current**
   - Update regularly
   - Remove outdated content
   - Add new information promptly

3. **Test continuously**
   - Verify answers are accurate
   - Check source citations
   - Refine based on feedback

4. **Organize well**
   - Use clear naming
   - Tag appropriately
   - Structure logically

### For Multiple Minds

1. **Define clear boundaries**
   - Each Mind has a specific domain
   - Avoid overlap between Minds
   - Document Mind purposes

2. **Manage access**
   - Control who can use each Mind
   - Set appropriate permissions
   - Monitor usage

3. **Maintain consistency**
   - Use similar structure across Minds
   - Standardize naming conventions
   - Keep documentation updated

## Troubleshooting Training Issues

### Common Problems

**Issue: Training takes too long**
- **Solution**: Reduce source size, split into smaller Minds
- **Check**: File sizes and document complexity

**Issue: Answers are inaccurate**
- **Solution**: Verify source quality, check for conflicts
- **Test**: Ask known questions, verify responses

**Issue: Mind not being used**
- **Solution**: Ensure Mind is enabled, check settings
- **Verify**: Mind is active for current query

**Issue: Sources not found**
- **Solution**: Check URLs are accessible, files are valid
- **Verify**: All sources uploaded correctly

## Next Steps

- **Learn about Automations**: [`automations-webhooks-api-magnets.md`](automations-webhooks-api-magnets.md)
- **Explore Models**: [`models-allowances-and-byok.md`](models-allowances-and-byok.md)
- **Understand Security**: [`security-privacy-and-data.md`](security-privacy-and-data.md)

---

**Official Documentation**: [documentation.triplo.ai/using-triplo-ai/training](https://documentation.triplo.ai/using-triplo-ai/training)
