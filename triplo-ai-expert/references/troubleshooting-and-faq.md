# Troubleshooting and FAQ

## Troubleshooting Playbook

When something "doesn't work" in Triplo AI, follow this systematic approach:

### Step 1: Identify the Issue

**Common issue categories**:
- Installation/Activation
- Device limits
- SmartPrompts not working
- Training not affecting outputs
- Token limit errors
- Performance issues
- Connection problems
- Feature-specific issues

### Step 2: Run Diagnostic Checks

**Checklist**:
- [ ] Is Triplo AI running?
- [ ] Is device activated?
- [ ] Is internet connection stable?
- [ ] Are settings correct?
- [ ] Is the feature enabled?
- [ ] Are there error messages?

### Step 3: Apply Fixes

**Apply fixes in order**:
1. Quick fixes (restart, recheck settings)
2. Common solutions (reinstall, clear cache)
3. Advanced solutions (contact support, check logs)

### Step 4: Verify Resolution

**After applying fix**:
- Test the issue is resolved
- Check for new issues
- Document what worked
- Share solution if helpful

## Common Issues and Solutions

### Installation Issues

**Issue: Installer won't run**

**Possible causes**:
- Security software blocking
- Insufficient permissions
- Corrupted download

**Solutions**:
1. Run installer as administrator (Windows)
2. Disable antivirus temporarily
3. Redownload installer
4. Check system requirements

**Issue: Installation fails**

**Possible causes**:
- Incompatible OS version
- Insufficient disk space
- Missing dependencies

**Solutions**:
1. Check OS compatibility
2. Free up disk space
3. Install required dependencies
4. Try different installation method

### Activation Issues

**Issue: Can't sign in**

**Possible causes**:
- Wrong credentials
- Account suspended
- Network issues

**Solutions**:
1. Verify email and password
2. Reset password if needed
3. Check account status
4. Try different network

**Issue: Device not activating**

**Possible causes**:
- Device limit reached
- Activation server issues
- Account problems

**Solutions**:
1. Check device limit in account
2. Remove unused devices
3. Upgrade plan if needed
4. Contact support

**Issue: Token allowance not showing**

**Possible causes**:
- Subscription not active
- Billing issue
- Sync delay

**Solutions**:
1. Verify subscription is active
2. Check billing status
3. Wait for sync (may take time)
4. Refresh account

### Device Limit Issues

**Issue: Reached device limit**

**Possible causes**:
- Too many devices activated
- Old devices not removed
- Plan limit too low

**Solutions**:
1. Remove unused devices from account
2. Upgrade plan for more devices
3. Contact support for special cases

**Issue: Can't add new device**

**Possible causes**:
- Device limit reached
- Device already activated
- Account issues

**Solutions**:
1. Check current device count
2. Remove old devices
3. Verify device not already activated
4. Contact support

### SmartPrompt Issues

**Issue: SmartPrompt not behaving as expected**

**Possible causes**:
- Poor prompt design
- Wrong context
- Model limitations
- Conflicting settings

**Solutions**:
1. Review prompt instructions
2. Check context is correct
3. Try different model
4. Simplify prompt

**Issue: SmartPrompt not found**

**Possible causes**:
- Deleted SmartPrompt
- Sync issue
- Wrong name

**Solutions**:
1. Check SmartPrompt library
2. Refresh library
3. Verify exact name
4. Recreate if needed

**Issue: Custom SmartPrompt not working**

**Possible causes**:
- Invalid prompt format
- Missing required fields
- Syntax errors

**Solutions**:
1. Validate prompt syntax
2. Check required fields
3. Test with simple input
4. Use template as reference

### Training Issues

**Issue: Training not affecting outputs**

**Possible causes**:
- Mind not enabled
- Wrong Mind selected
- Training incomplete
- Irrelevant content

**Solutions**:
1. Enable Mind in settings
2. Select correct Mind
3. Verify training completed
4. Check content relevance

**Issue: Training takes too long**

**Possible causes**:
- Large file size
- Many documents
- Server load

**Solutions**:
1. Reduce file size
2. Train in smaller batches
3. Wait for off-peak hours
4. Contact support if excessive

**Issue: Can't upload files for training**

**Possible causes**:
- File format not supported
- File too large
- Upload error

**Solutions**:
1. Check supported formats
2. Compress or split large files
3. Try different file
4. Check internet connection

### Token Limit Issues

**Issue: Ran out of tokens**

**Possible causes**:
- Exceeded monthly allowance
- High usage
- Token leak

**Solutions**:
1. Wait for monthly reset
2. Upgrade plan
3. Use BYOK with own keys
4. Use local models

**Issue: Token counting seems wrong**

**Possible causes**:
- Misunderstanding of token count
- Hidden usage
- Counting error

**Solutions**:
1. Check usage dashboard
2. Understand token pricing
3. Review recent activity
4. Contact support if discrepancy

### Performance Issues

**Issue: Triplo is slow**

**Possible causes**:
- High server load
- Slow internet
- Resource constraints
- Large context

**Solutions**:
1. Check internet speed
2. Reduce context size
3. Use faster model
4. Close other applications

**Issue: Responses are poor quality**

**Possible causes**:
- Wrong model selected
- Poor prompt
- Insufficient context
- Model limitations

**Solutions**:
1. Try different model
2. Improve prompt
3. Provide more context
4. Use relevant Mind

### Connection Issues

**Issue: Can't connect to Triplo servers**

**Possible causes**:
- Internet down
- Firewall blocking
- Server outage
- DNS issues

**Solutions**:
1. Check internet connection
2. Disable firewall temporarily
3. Check Triplo status page
4. Try different network

**Issue: Webhook/Automation not working**

**Possible causes**:
- Wrong URL
- Authentication failed
- Server down
- Invalid JSON

**Solutions**:
1. Verify webhook URL
2. Check authentication
3. Test webhook endpoint
4. Validate JSON structure

### Local Model Issues

**Issue: Can't connect to local model**

**Possible causes**:
- Server not running
- Wrong endpoint URL
- Firewall blocking
- Port conflict

**Solutions**:
1. Start local model server
2. Verify endpoint URL
3. Check firewall settings
4. Try different port

**Issue: Local model slow**

**Possible causes**:
- Insufficient hardware
- Large model size
- No GPU acceleration
- High quantization

**Solutions**:
1. Use smaller model
2. Enable GPU acceleration
3. Quantize model
4. Reduce context

## FAQ

### General Questions

**Q: What is Triplo AI?**
A: Triplo AI is a system-wide AI assistant that works across any application on your desktop and mobile devices without requiring individual app integrations.

**Q: How much does Triplo cost?**
A: Pricing varies by plan. Check [triplo.ai](https://triplo.ai) for current pricing. Free tier available with limited features.

**Q: What platforms does Triplo support?**
A: Windows, macOS, iOS, and Android.

**Q: Can I use Triplo offline?**
A: Yes, if you set up local models. Cloud models require internet connection.

### Installation and Setup

**Q: How do I install Triplo?**
A: Download from [triplo.ai](https://triplo.ai) and follow the installation wizard for your platform.

**Q: How do I activate my device?**
A: Sign in with your Triplo account after installation. The device will be automatically activated.

**Q: Can I use Triplo on multiple devices?**
A: Yes, depending on your plan. Check your account settings for device limit.

### Features and Usage

**Q: What are SmartPrompts?**
A: SmartPrompts are reusable prompt templates that ensure consistent, high-quality AI outputs for specific tasks.

**Q: How do I create a custom SmartPrompt?**
A: Go to SmartPrompts library, click "Create New SmartPrompt," write your prompt, and save.

**Q: What is Training/Minds?**
A: Training lets you build knowledge bases (Minds) from your documents, URLs, and other sources to ground AI responses in your actual information.

**Q: Can I use my own API keys?**
A: Yes, Triplo supports BYOK (Bring Your Own Keys) for OpenAI and OpenRouter.

### Models and Performance

**Q: What models does Triplo support?**
A: Native models, OpenRouter models (100+), and local models. See [`models-allowances-and-byok.md`](models-allowances-and-byok.md) for details.

**Q: How many tokens do I get?**
A: Depends on your plan. Pro tier typically includes 2M+ tokens per device per month.

**Q: What happens when I run out of tokens?**
A: Wait for monthly reset, upgrade plan, use BYOK, or use local models.

**Q: Should I use local or cloud models?**
A: Use local for privacy and offline use. Use cloud for quality and speed. See [`local-models-strengths.md`](local-models-strengths.md) for guidance.

### Privacy and Security

**Q: Is my data safe with Triplo?**
A: Triplo uses industry-standard security measures. Data sent to cloud models is processed according to provider policies. Use local models for complete privacy.

**Q: Can Triplo see my content?**
A: With local models, no. With cloud models, content is sent to model providers. Training data is stored securely on Triplo servers.

**Q: How do I delete my data?**
A: Contact Triplo support for account deletion, delete Minds from interface, or clear local data manually.

### Troubleshooting

**Q: Triplo isn't responding. What should I do?**
A: Check internet connection, restart Triplo, check for updates, or contact support.

**Q: I'm getting an error message. What does it mean?**
A: Error messages usually indicate the issue. Check the FAQ or contact support with the exact error message.

**Q: How do I report a bug?**
A: Contact Triplo support with details about the issue, steps to reproduce, and your system information.

## Getting Help

### Self-Service Resources

**Documentation**:
- [documentation.triplo.ai](https://documentation.triplo.ai)
- Comprehensive guides and tutorials

**Changelog**:
- Check for known issues and fixes
- See what's new in each version

**Community**:
- Check if others have similar issues
- Share solutions and workarounds

### Contacting Support

**When to contact support**:
- Issue not resolved by troubleshooting
- Error messages unclear
- Account or billing issues
- Feature requests

**Information to provide**:
1. Describe the issue clearly
2. Steps to reproduce
3. Expected vs. actual behavior
4. System information (OS, version)
5. Error messages (if any)

**How to contact**:
- Through Triplo app (Help → Contact Support)
- Via support email (check website)
- Through community forums

## Best Practices

### For Effective Troubleshooting

1. **Be systematic**
   - Follow the playbook
   - Check items in order
   - Document what you try

2. **Gather information**
   - Note error messages
   - Record steps to reproduce
   - Check system status

3. **Try simple fixes first**
   - Restart application
   - Check internet connection
   - Verify settings

4. **Know when to escalate**
   - If issue persists after trying solutions
   - If error is unclear
   - If it affects critical functionality

### For Preventing Issues

1. **Keep software updated**
   - Update Triplo regularly
   - Update operating system
   - Update dependencies

2. **Monitor usage**
   - Track token consumption
   - Watch for unusual activity
   - Check device list

3. **Maintain good practices**
   - Use appropriate models
   - Design good prompts
   - Secure your account

## Next Steps

- **Check Changelog**: [`changelog-roadmap-and-support.md`](changelog-roadmap-and-support.md)
- **Learn about Learning Paths**: [`learning-paths-and-resources.md`](learning-paths-and-resources.md)
- **Explore Getting Started**: [`getting-started-install-activate.md`](getting-started-install-activate.md)

---

**Official Documentation**: [documentation.triplo.ai/troubleshooting](https://documentation.triplo.ai/troubleshooting)
