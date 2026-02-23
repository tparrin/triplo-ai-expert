# Context Awareness and Sources

## What is Context Awareness?

Triplo AI's **Context Awareness** allows it to read and understand content directly from your screen, clipboard, and files. This means the AI sees exactly what you see, without requiring copy-pasting or manual input.

### Awareness Modes

Triplo AI provides three main awareness modes:

| Mode | What It Reads | When To Use |
|------|----------------|--------------|
| **Context** | Entire active window or document | When you want AI to analyze full content |
| **Selection** | Text you've highlighted | When focusing on specific content |
| **Clipboard** | Current clipboard content | When working with copied content |

## Using Awareness Modes

### 1. Context Mode (Full Window)

**What it does**: Reads the entire content of your active window or document.

**How to use**:
1. Open or activate the document/application
2. Trigger Triplo AI
3. Select "Context" mode (default)
4. Triplo reads the entire window content
5. Ask questions or run SmartPrompts

**Best for**:
- Analyzing full documents
- Understanding complete context
- Getting summaries of entire files
- Finding information across documents

**Example workflows**:
- Open a research paper → Trigger Triplo → "What are the key findings?"
- Open a long email thread → Trigger Triplo → "Summarize this conversation"
- Open a spreadsheet → Trigger Triplo → "Analyze trends in this data"

### 2. Selection Mode

**What it does**: Reads only the text you've highlighted or selected.

**How to use**:
1. Select text in any application
2. Trigger Triplo AI
3. Triplo automatically uses selected text
4. Process with prompt or SmartPrompt

**Best for**:
- Focusing on specific passages
- Processing excerpts
- Quick analysis of selected content
- Targeted rewriting or editing

**Example workflows**:
- Select a paragraph → Trigger Triplo → "Rewrite this more professionally"
- Select code snippet → Trigger Triplo → "Explain this code"
- Select customer feedback → Trigger Triplo → "Extract action items"

### 3. Clipboard Mode

**What it does**: Uses whatever content is currently in your clipboard.

**How to use**:
1. Copy content to clipboard (`Ctrl/Cmd + C`)
2. Trigger Triplo AI
3. Select "Clipboard" mode
4. Triplo uses clipboard as context
5. Process with prompt or SmartPrompt

**Best for**:
- Working with content from multiple sources
- Processing copied content
- Combining information from different apps
- Quick content transfer

**Example workflows**:
- Copy support ticket → Trigger Triplo → "Convert to blog post"
- Copy meeting notes → Trigger Triplo → "Extract action items"
- Copy product description → Trigger Triplo → "Generate marketing copy"

## Working with Files

### File Upload

Triplo AI can process various file types directly:

**Supported File Types**:
- **Text**: .txt, .md, .csv, .json
- **Documents**: .pdf, .docx, .doc
- **Spreadsheets**: .xlsx, .xls, .csv
- **Presentations**: .pptx, .ppt
- **Code**: .py, .js, .html, .css, .java, .cpp, etc.

**How to upload files**:
1. Trigger Triplo AI
2. Click attachment icon or "Upload File"
3. Select file from your device
4. Triplo processes the file
5. Ask questions or run SmartPrompts

**Best practices**:
- Use appropriate file formats
- Keep files under size limits (check current limits)
- Organize related files together
- Use descriptive filenames

### File Analysis Workflows

**Document Analysis**:
1. Upload PDF report
2. Ask: "What are the key metrics?"
3. Follow up: "How do they compare to last quarter?"

**Code Review**:
1. Upload code file
2. Ask: "Review for security issues"
3. Follow up: "Suggest improvements"

**Data Extraction**:
1. Upload spreadsheet
2. Ask: "Extract all customer emails"
3. Follow up: "Categorize by region"

## Working with Images

### Image Upload

Triplo AI can analyze images and extract information:

**Supported Image Types**:
- **Screenshots**: .png, .jpg, .jpeg
- **Photos**: .png, .jpg, .jpeg, .gif
- **Scanned documents**: .png, .jpg, .pdf (with OCR)

**How to upload images**:
1. Trigger Triplo AI
2. Click image attachment icon
3. Select image from your device
4. Triplo analyzes the image
5. Ask questions or run SmartPrompts

**Use cases**:
- **Screenshot analysis**: Analyze UI/UX, extract text from screenshots
- **Document scanning**: Extract text from scanned documents
- **Photo analysis**: Describe images, extract information
- **Chart/graph analysis**: Read data from visualizations

### Image Analysis Workflows

**Screenshot to Text**:
1. Take screenshot of error message
2. Upload to Triplo
3. Ask: "What does this error mean?"
4. Get explanation and solutions

**Chart Data Extraction**:
1. Screenshot chart or graph
2. Upload to Triplo
3. Ask: "Extract all data points"
4. Get structured data

**Document OCR**:
1. Scan document to image
2. Upload to Triplo
3. Ask: "Extract all text"
4. Get searchable text

## Scraping Web Pages

### Web Page Content Extraction

Triplo AI can read content from web pages:

**How to scrape a webpage**:
1. Open webpage in browser
2. Trigger Triplo AI
3. Triplo reads the active webpage content
4. Ask questions or run SmartPrompts

**What Triplo extracts**:
- Main content (articles, blog posts)
- Headings and structure
- Text content (not ads or navigation)
- Links and references

**Best for**:
- Article summarization
- Content extraction
- Research gathering
- Competitive analysis

**Example workflows**:
- Open blog post → Trigger Triplo → "Summarize key points"
- Open product page → Trigger Triplo → "Extract features and pricing"
- Open competitor site → Trigger Triplo → "Analyze their content strategy"

### Limitations

**What Triplo cannot do**:
- Access password-protected content
- Read dynamic JavaScript content
- Access behind paywalls
- Scrape entire sites (single pages only)

**Workarounds**:
- Log in first, then trigger Triplo
- Take screenshots of dynamic content
- Copy content manually if needed

## Scraping YouTube Subtitles

### YouTube Video Analysis

Triplo AI can extract and analyze YouTube video subtitles:

**How to analyze YouTube videos**:
1. Open YouTube video in browser
2. Trigger Triplo AI
3. Triplo extracts video subtitles
4. Ask questions or run SmartPrompts

**What you can do**:
- Summarize video content
- Extract key points
- Create transcripts
- Find specific information
- Generate show notes

**Example workflows**:
- Open tutorial video → Trigger Triplo → "Summarize the tutorial"
- Open interview video → Trigger Triplo → "Extract quotes about X"
- Open product review → Trigger Triplo → "List pros and cons"

**Best practices**:
- Use videos with subtitles (auto-generated or manual)
- Longer videos provide more context
- Combine with video description for better results

## Using Desktop and Mobile Content

### Desktop Content

**Sources**:
- Active windows and applications
- Selected text
- Clipboard content
- Uploaded files and images
- Webpages in browser

**Workflow patterns**:
- Select → Trigger → Process
- Window active → Trigger → Analyze
- Copy → Trigger → Transform
- Upload → Trigger → Extract

### Mobile Content

**Sources**:
- Active app content
- Selected text
- Clipboard content
- Uploaded files and images
- Webpages in browser

**Workflow patterns**:
- Share to Triplo from any app
- Select text → Share → Triplo
- Copy content → Open Triplo → Process
- Upload file → Ask questions

## Advanced Context Usage

### Combining Multiple Sources

You can combine context from multiple sources:

**Example 1: Document + Selection**
1. Upload document (Context mode)
2. Select specific section (Selection mode)
3. Ask: "How does this section relate to the whole document?"

**Example 2: Webpage + Clipboard**
1. Open webpage (Context mode)
2. Copy related info to clipboard
3. Ask: "Compare this webpage to the clipboard content"

**Example 3: Multiple Files**
1. Upload File A
2. Upload File B
3. Ask: "Find differences between these files"

### Context Persistence

Triplo AI can maintain context across multiple queries:

**How it works**:
1. First query uses initial context
2. Follow-up queries reference previous context
3. You can add new context mid-conversation
4. Triplo combines all available context

**Best for**:
- Multi-step analysis
- Iterative refinement
- Complex queries requiring multiple pieces of information

## Best Practices

### For Effective Context

1. **Be specific about what you want analyzed**
   - "Analyze the selected paragraph" vs. "Analyze this"

2. **Use appropriate awareness mode**
   - Selection for focused content
   - Context for full documents
   - Clipboard for copied content

3. **Provide clear instructions**
   - Tell Triplo what to look for
   - Specify output format
   - Define constraints

4. **Iterate and refine**
   - Start with broad questions
   - Narrow down with follow-ups
   - Add more context as needed

### For File Handling

1. **Use appropriate file formats**
   - PDF for documents
   - CSV for data
   - Markdown for text

2. **Keep files organized**
   - Descriptive filenames
   - Logical folder structure
   - Related files together

3. **Check file size limits**
   - Large files may timeout
   - Split large documents if needed
   - Compress when possible

### For Web Scraping

1. **Focus on content pages**
   - Articles and blog posts
   - Product pages
   - Documentation

2. **Avoid scraping sensitive content**
   - Password-protected pages
   - Personal accounts
   - Behind paywalls

3. **Combine with other sources**
   - Webpage + uploaded file
   - Multiple webpages
   - Webpage + clipboard

## Troubleshooting Context Issues

### Common Problems

**Issue: Context not detected**
- **Solution**: Ensure window is active, text is selected, or file is uploaded
- **Check**: Context panel shows what Triplo sees

**Issue: Wrong content being read**
- **Solution**: Verify correct awareness mode is selected
- **Check**: Selection is active, window is focused

**Issue: File upload fails**
- **Solution**: Check file format and size limits
- **Verify**: File is not corrupted

**Issue: Webpage scraping doesn't work**
- **Solution**: Ensure page is fully loaded, try refreshing
- **Check**: Page is not password-protected

## Next Steps

- **Learn about Training**: [`training-and-knowledge-bases.md`](training-and-knowledge-bases.md)
- **Explore Automations**: [`automations-webhooks-api-magnets.md`](automations-webhooks-api-magnets.md)
- **Understand Models**: [`models-allowances-and-byok.md`](models-allowances-and-byok.md)

---

**Official Documentation**: [documentation.triplo.ai/using-triplo-ai/context-awareness](https://documentation.triplo.ai/using-triplo-ai/context-awareness)
