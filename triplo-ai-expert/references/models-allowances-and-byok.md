# Models, Allowances, and BYOK

## Included Models

Triplo AI provides access to multiple AI models, each optimized for different use cases.

### Native Models

**Included with Triplo Pro**:
- Generous monthly token allowance per device (typically 2M+ tokens)
- No additional cost for included models
- Optimized for general-purpose tasks

**Common native models**:
- **GPT-4**: Advanced reasoning, complex tasks
- **GPT-3.5-Turbo**: Fast, cost-effective for simple tasks
- **Claude**: Strong at analysis and writing
- **Other models**: Check current offerings in Triplo settings

### OpenRouter Integration

**Access to 100+ models** via OpenRouter:
- Specialized models for specific tasks
- Cost-effective alternatives
- Latest model releases
- Custom fine-tuned models

**Popular OpenRouter models**:
- **Anthropic Claude**: Strong reasoning and writing
- **Meta Llama**: Open-source, cost-effective
- **Google PaLM**: Multimodal capabilities
- **Mistral**: Efficient, fast
- **Many others**: See OpenRouter for full list

### Local Models

**Run models on your own hardware**:
- Complete privacy
- No API costs
- Offline capability
- Custom model support

**Popular local models**:
- **Llama 2/3**: Meta's open-source models
- **Mistral**: Efficient and fast
- **Phi**: Microsoft's compact models
- **Others**: See [`local-models-strengths.md`](local-models-strengths.md)

## Token Allowances

### What are Tokens?

Tokens are the basic units of text that AI models process:
- Roughly 1 token ≈ 4 characters in English
- 1,000 tokens ≈ 750 words
- Both input and output count toward allowance

### Monthly Allowances

| Plan | Tokens Per Device | Notes |
|-------|-------------------|-------|
| **Free** | Limited | Basic models only |
| **Pro** | 2,000,000+ | All models included |
| **Enterprise** | Custom | Unlimited or negotiated |

**Allowance details**:
- Per device, not per account
- Resets monthly
- Does not roll over
- Check current allowance in Triplo settings

### Managing Token Usage

**Monitor usage**:
- Check usage dashboard in Triplo
- Track consumption by device
- View usage by model type
- Set alerts if available

**Optimize usage**:
- Use appropriate model for task
- Minimize unnecessary context
- Use cheaper models for simple tasks
- Cache results when possible

**When you run out**:
- Wait for monthly reset
- Upgrade plan
- Use BYOK with your own keys
- Use local models (no tokens)

## Bring Your Own Keys (BYOK)

### What is BYOK?

BYOK allows you to use your own API keys for OpenAI or OpenRouter instead of Triplo's included models.

### Why Use BYOK?

**Use BYOK when**:
- You have existing API credits
- Need specific model not included
- Want more control over costs
- Have enterprise agreements
- Prefer direct billing

**Don't use BYOK when**:
- Triplo's allowance is sufficient
- Included models meet your needs
- Want simplicity
- Prefer Triplo's billing

### Setting Up BYOK

**OpenAI BYOK**:
1. Get API key from OpenAI platform
2. Open Triplo settings
3. Go to Models → BYOK
4. Select "OpenAI"
5. Enter API key
6. Test connection
7. Save

**OpenRouter BYOK**:
1. Get API key from OpenRouter
2. Open Triplo settings
3. Go to Models → BYOK
4. Select "OpenRouter"
5. Enter API key
6. Test connection
7. Save

### BYOK Considerations

**Cost management**:
- You're billed directly by provider
- Monitor your API usage
- Set spending limits if available
- Track costs separately from Triplo

**Model availability**:
- Access to provider's full catalog
- Latest models immediately available
- Custom fine-tunes if supported

**Reliability**:
- Depends on provider uptime
- May have different latency
- Check provider status pages

## Model Selection Guide

### Choosing the Right Model

**By Task Type**:

| Task | Recommended Model | Why |
|-------|-------------------|------|
| **Simple Q&A** | GPT-3.5-Turbo, Llama 2 | Fast, cost-effective |
| **Complex reasoning** | GPT-4, Claude | Advanced understanding |
| **Writing/Editing** | Claude, GPT-4 | Strong language skills |
| **Code generation** | GPT-4, Claude | Good at programming |
| **Analysis** | Claude, GPT-4 | Deep understanding |
| **Translation** | GPT-4, specialized models | Multilingual support |
| **Privacy-sensitive** | Local models | No data leaves device |
| **Cost-sensitive** | Llama 2, Mistral | Low cost per token |

### Decision Framework

**Ask these questions**:

1. **How complex is the task?**
   - Simple → Use cheaper model
   - Complex → Use powerful model

2. **Is privacy a concern?**
   - Yes → Use local model
   - No → Use cloud model

3. **What's the budget?**
   - Limited → Use cost-effective model
   - Flexible → Use best model for task

4. **Is speed important?**
   - Yes → Use fast model
   - No → Use most capable model

5. **Do you have specific requirements?**
   - Yes → Use specialized model via OpenRouter
   - No → Use general-purpose model

### Model Comparison

**GPT-4**:
- **Strengths**: Reasoning, complex tasks, code
- **Weaknesses**: Slower, more expensive
- **Best for**: Complex analysis, coding, writing

**GPT-3.5-Turbo**:
- **Strengths**: Fast, cost-effective
- **Weaknesses**: Less capable
- **Best for**: Simple tasks, quick responses

**Claude**:
- **Strengths**: Writing, analysis, long context
- **Weaknesses**: May be slower
- **Best for**: Content creation, document analysis

**Llama 2**:
- **Strengths**: Cost-effective, open-source
- **Weaknesses**: Less capable than GPT-4
- **Best for**: Budget-conscious tasks

**Mistral**:
- **Strengths**: Fast, efficient
- **Weaknesses**: Newer, less tested
- **Best for**: Speed-critical tasks

## Advanced Model Configuration

### Per-Device Model Configuration

**Why configure per device?**
- Different devices have different use cases
- Optimize for device capabilities
- Manage costs across devices
- Tailor to user preferences

**How to configure**:
1. Open Triplo on device
2. Go to Settings → Models
3. Select default model for this device
4. Enable/disable specific models
5. Save settings

**Example configurations**:
- **Work laptop**: GPT-4 for complex tasks
- **Personal laptop**: GPT-3.5-Turbo for speed
- **Mobile device**: Optimized mobile model

### Model Parameters

**Adjustable parameters** (if available):

**Temperature**:
- **Low (0.1-0.3)**: More deterministic, focused
- **Medium (0.5-0.7)**: Balanced
- **High (0.8-1.0)**: More creative, varied

**Max Tokens**:
- Limit response length
- Control costs
- Manage context

**Top P / Top K**:
- Control diversity of responses
- Lower = more focused
- Higher = more varied

## Cost Optimization

### Strategies to Reduce Costs

1. **Use appropriate models**
   - Don't use GPT-4 for simple tasks
   - Use cheaper models when possible

2. **Optimize prompts**
   - Be concise and specific
   - Avoid unnecessary context
   - Use system messages effectively

3. **Cache results**
   - Store responses for reuse
   - Avoid regenerating same content

4. **Use local models**
   - No API costs
   - Best for privacy-sensitive tasks

5. **Monitor usage**
   - Track token consumption
   - Identify expensive patterns
   - Adjust accordingly

### Cost Comparison

**Approximate costs** (check current pricing):

| Model | Cost per 1K tokens | Notes |
|--------|---------------------|-------|
| **GPT-4** | $0.03-0.06 | Most expensive |
| **GPT-3.5-Turbo** | $0.001-0.002 | Very cost-effective |
| **Claude** | $0.003-0.015 | Mid-range |
| **Llama 2** | $0.0001-0.001 | Very cheap |
| **Mistral** | $0.0001-0.0007 | Very cheap |
| **Local models** | $0 | Hardware cost only |

## Troubleshooting

### Common Issues

**Issue: Ran out of tokens**
- **Solution**: Wait for reset, upgrade plan, use BYOK, or use local models
- **Check**: Usage dashboard for consumption details

**Issue: Model not available**
- **Solution**: Check if model is included, use BYOK, or use alternative
- **Verify**: Model is enabled in settings

**Issue: BYOK connection failing**
- **Solution**: Verify API key, test connection directly
- **Check**: API key is valid and has credits

**Issue: Poor response quality**
- **Solution**: Try different model, adjust parameters, improve prompt
- **Test**: Multiple models to find best fit

## Next Steps

- **Learn about OpenRouter models**: [`openrouter-models-strengths.md`](openrouter-models-strengths.md)
- **Explore local models**: [`local-models-strengths.md`](local-models-strengths.md)
- **Set up local models**: [`local-llms-setup-desktop-mobile.md`](local-llms-setup-desktop-mobile.md)

---

**Official Documentation**: [documentation.triplo.ai/using-triplo-ai/models](https://documentation.triplo.ai/using-triplo-ai/models)
