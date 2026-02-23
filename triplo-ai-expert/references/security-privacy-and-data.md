# Security, Privacy, and Data

## Data Handling Approach

Triplo AI takes a **transparent approach** to data handling, with clear policies on what data is collected, how it's stored, and who has access.

### Core Principles

| Principle | What It Means |
|-----------|----------------|
| **Transparency** | Clear documentation of data practices |
| **Control** | You control your data |
| **Privacy** | Respect for user privacy |
| **Security** | Industry-standard security measures |

## What Data is Collected

### Account Data

**Information collected**:
- Email address (for account)
- Device information (for activation)
- Usage statistics (for improvement)
- Subscription details (for billing)

**Purpose**:
- Account management
- Device activation and management
- Service improvement
- Billing and support

### Usage Data

**Information collected**:
- Token usage (for allowance tracking)
- Model usage (for optimization)
- Feature usage (for improvement)
- Error logs (for debugging)

**Purpose**:
- Track token allowances
- Improve service quality
- Fix bugs and issues
- Optimize performance

### Content Data

**What happens to your content**:

**Local models**:
- Data stays on your device
- No data sent to external servers
- Complete privacy

**Cloud models**:
- Data sent to model provider
- Processed according to provider's policies
- Not stored by Triplo (unless using features that require storage)

**Training/Minds**:
- Documents uploaded to Triplo servers
- Used to build knowledge bases
- Stored securely
- You control access

## Data Storage Locations

### Local Storage

**Desktop**:
- **Windows**: `%APPDATA%\Triplo AI\`
- **macOS**: `~/Library/Application Support/Triplo AI/`
- **Linux**: `~/.config/triplo-ai/`

**Stored locally**:
- Application settings
- Local model files (if downloaded)
- Conversation history (if enabled)
- Cache and temporary files

**Mobile**:
- **iOS**: App sandbox (managed by iOS)
- **Android**: App data directory (managed by Android)

**Stored locally**:
- App settings
- Local model files (if downloaded)
- Conversation history (if enabled)
- Cache and temporary files

### Cloud Storage

**Triplo servers**:
- Account information
- Device associations
- Training/Minds data
- Usage statistics

**Storage locations**:
- Secure cloud infrastructure
- Encrypted at rest
- Access controls in place

**Model providers**:
- Content sent to model providers (OpenAI, OpenRouter, etc.)
- Stored according to provider's policies
- Check provider's privacy policy for details

## Privacy Features

### Local Models

**Complete privacy**:
- Data never leaves your device
- No external API calls
- Offline capability
- Full control

**Best for**:
- Sensitive documents
- Confidential work
- Privacy-critical environments
- Offline use

### Data Retention

**Triplo's policy**:
- **Content**: Not stored (unless using Training/Minds)
- **Conversations**: Stored locally (if enabled), not on Triplo servers
- **Training data**: Stored securely, you control access
- **Usage data**: Retained for service improvement

**Model providers' policies**:
- Vary by provider
- Check provider's privacy policy
- Typically retain data for improvement (can opt out)

### Data Deletion

**How to delete your data**:

**Account deletion**:
1. Contact Triplo support
2. Request account deletion
3. Confirm deletion
4. All account data removed

**Training/Minds deletion**:
1. Go to Training/Minds section
2. Select Mind to delete
3. Confirm deletion
4. All data removed

**Local data deletion**:
- Delete local storage directories
- Clear app cache
- Uninstall application

## Security Measures

### Encryption

**Data in transit**:
- HTTPS/TLS encryption
- Secure connections
- Certificate validation

**Data at rest**:
- Encrypted storage
- Secure cloud infrastructure
- Access controls

### Access Controls

**Account security**:
- Password requirements
- Two-factor authentication (if available)
- Device management
- Session management

**Data access**:
- Role-based access
- Audit logs
- Regular security reviews

### Compliance

**Standards**:
- GDPR compliance (for EU users)
- CCPA compliance (for California users)
- Industry best practices
- Regular security audits

## Privacy Settings

### Conversation History

**Control what's stored**:

**Settings options**:
- **Store conversations locally**: Enable/disable
- **Retention period**: How long to keep
- **Auto-delete**: Delete after X days
- **Manual delete**: Delete specific conversations

**Recommendations**:
- Disable history for sensitive work
- Set short retention period
- Regularly clear history
- Review stored conversations

### Training Data Access

**Control who can access your Minds**:

**Access control options**:
- **Personal**: Only you
- **Team**: Share with team members
- **Public**: Make available to others (if supported)

**Best practices**:
- Keep sensitive Minds private
- Share only when necessary
- Review access regularly
- Remove access when no longer needed

### Data Sharing

**Opt-out options**:
- **Usage statistics**: Can opt out of data collection
- **Feature improvement**: Can opt out of analytics
- **Model training**: Check provider opt-out options

## Best Practices

### For Privacy

1. **Use local models for sensitive data**
   - Complete privacy
   - No data leaves device
   - Best for confidential work

2. **Review privacy settings**
   - Check conversation history settings
   - Review training data access
   - Opt out of unnecessary data collection

3. **Understand data flow**
   - Know where your data goes
   - Check provider policies
   - Make informed choices

4. **Regular cleanup**
   - Delete old conversations
   - Remove unused Minds
   - Clear cache regularly

### For Security

1. **Secure your account**
   - Use strong passwords
   - Enable 2FA if available
   - Monitor device access

2. **Keep software updated**
   - Update Triplo AI
   - Update operating system
   - Update inference engines

3. **Use secure connections**
   - HTTPS only
   - Avoid public Wi-Fi for sensitive work
   - Use VPN if needed

4. **Monitor for suspicious activity**
   - Check device list
   - Review usage logs
   - Report issues immediately

## Common Concerns

### "Is my data safe with Triplo?"

**Answer**: Triplo takes security seriously with:
- Industry-standard encryption
- Secure cloud infrastructure
- Access controls
- Regular security audits

**But**: Data sent to cloud models is processed by model providers according to their policies.

### "Can Triplo see my content?"

**Answer**: 
- **Local models**: No, data stays on your device
- **Cloud models**: Content sent to model providers, not stored by Triplo (unless using Training/Minds)
- **Training/Minds**: Stored securely on Triplo servers, you control access

### "Is my data used for training?"

**Answer**:
- **Triplo**: Usage statistics used for improvement (can opt out)
- **Model providers**: Check provider's policy (many use data for improvement, can often opt out)
- **Your content**: Not used to train public models (unless explicitly enabled)

### "Can I delete my data?"

**Answer**: Yes
- Contact support for account deletion
- Delete Minds from interface
- Clear local data manually

## When to Use Local vs. Cloud Models

### Use Local Models When

- **Privacy is critical**: Sensitive documents, confidential work
- **Offline needed**: No internet, air-gapped systems
- **Compliance required**: Data must stay on-premise
- **Cost savings**: High volume, budget constraints

### Use Cloud Models When

- **Quality is priority**: Need best possible performance
- **Speed is critical**: Real-time requirements
- **Complex tasks**: Need advanced reasoning
- **Convenience**: Want ready-to-use solution

## Compliance and Regulations

### GDPR (EU)

**Your rights**:
- Right to access your data
- Right to delete your data
- Right to data portability
- Right to opt out of processing

**How to exercise rights**:
- Contact Triplo support
- Submit GDPR request
- Provide necessary information

### CCPA (California)

**Your rights**:
- Right to know what data is collected
- Right to delete your data
- Right to opt out of sale
- Right to non-discrimination

**How to exercise rights**:
- Contact Triplo support
- Submit CCPA request
- Provide necessary information

## Troubleshooting

### Common Issues

**Issue: Concern about data privacy**
- **Solution**: Use local models, review settings, check provider policies
- **Action**: Enable local models, disable history, opt out of analytics

**Issue: Want to delete data**
- **Solution**: Contact support, delete Minds, clear local data
- **Action**: Follow deletion process, verify removal

**Issue: Suspicious activity**
- **Solution**: Check device list, change password, contact support
- **Action**: Remove unauthorized devices, secure account, report issue

## Next Steps

- **Learn about Training**: [`training-and-knowledge-bases.md`](training-and-knowledge-bases.md)
- **Understand Local Models**: [`local-llms-setup-desktop-mobile.md`](local-llms-setup-desktop-mobile.md)
- **Explore Troubleshooting**: [`troubleshooting-and-faq.md`](troubleshooting-and-faq.md)

---

**Official Documentation**: [documentation.triplo.ai/data-security-privacy](https://documentation.triplo.ai/data-security-privacy)
