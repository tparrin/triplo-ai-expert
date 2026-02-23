# UI, Triggering, and Hotkeys

## Triggering Triplo AI

Triplo AI is designed to be available **anywhere** on your system. You can trigger it from any application, browser, or context.

### Desktop Triggering Methods

#### 1. Global Hotkeys (Recommended)

**Default Hotkeys**:
- **Windows**: `Ctrl + Shift + T` (or custom)
- **macOS**: `Cmd + Shift + T` (or custom)

**Customizing Hotkeys**:
1. Open Triplo AI
2. Go to Settings → Hotkeys
3. Click on the hotkey field
4. Press your desired key combination
5. Save changes

**Best Practices**:
- Choose keys that don't conflict with other apps
- Use memorable combinations
- Consider ergonomics (avoid awkward finger stretches)

#### 2. Menu Bar / System Tray

**Windows**:
- Click Triplo icon in system tray (bottom right)
- Select "Open Triplo" from menu

**macOS**:
- Click Triplo icon in menu bar (top right)
- Select "Open Triplo" from menu

#### 3. Application Menu

Some applications integrate Triplo directly:
- Look for "Ask Triplo" or "AI Assistant" in app menus
- Right-click context menus may include Triplo options

#### 4. Browser Extension

If using the Triplo browser extension:
- Click the Triplo icon in your browser toolbar
- Select text on a webpage, then right-click → "Ask Triplo"

### Mobile Triggering

#### iOS
- **App Widget**: Add Triplo widget to home screen
- **Share Sheet**: In any app, tap Share → Triplo
- **App Icon**: Open Triplo app directly

#### Android
- **Quick Settings**: Add Triplo to quick settings panel
- **Share Menu**: In any app, tap Share → Triplo
- **App Icon**: Open Triplo app directly

## Main Interfaces

### Desktop Interface

#### 1. Main Window

When triggered, Triplo opens a floating window with:

**Input Section**:
- Text input field for prompts
- Context indicator (shows what Triplo is "aware" of)
- Model selector
- SmartPrompt dropdown

**Output Section**:
- AI response display
- Copy button
- Regenerate option
- Save to notes option

**Action Bar**:
- Voice input toggle
- Attachment options (files, images)
- History access
- Settings access

#### 2. Context Panel

Shows what Triplo is currently aware of:
- **Selection**: Text you've selected
- **Window**: Content of the active window
- **Clipboard**: Current clipboard content

#### 3. SmartPrompt Library

Browse and select from:
- Built-in SmartPrompts
- Your custom SmartPrompts
- Community SmartPrompts (if available)

#### 4. Training/Minds Panel

Access your knowledge bases:
- View all trained Minds
- See what's in each Mind
- Enable/disable Minds for current session

### Mobile Interface

#### iOS/Android App

**Home Screen**:
- Quick prompt input
- Recent conversations
- SmartPrompt shortcuts
- Model selector

**Conversation View**:
- Chat-style interface
- Voice input button
- Context awareness indicator
- Action buttons (copy, share, save)

**Navigation**:
- Conversations history
- SmartPrompts library
- Training/Minds
- Settings

## Hotkeys for Instant Workflows

### "Run Prompts Instantly" Feature

Triplo allows you to assign hotkeys to specific SmartPrompts for instant execution.

**Setting Up Instant Hotkeys**:
1. Go to SmartPrompts library
2. Select a SmartPrompt
3. Click "Assign Hotkey"
4. Press desired key combination
5. Save

**Use Cases**:
- `Ctrl + Alt + S`: Summarize selected text
- `Ctrl + Alt + E`: Explain selected code
- `Ctrl + Alt + R`: Rewrite selected text
- `Ctrl + Alt + T`: Translate to target language

**Best Practices**:
- Use descriptive hotkey combinations
- Document your hotkey assignments
- Group related prompts with similar hotkeys

### Global Hotkey Reference

| Action | Default Hotkey | Description |
|--------|----------------|-------------|
| **Open Triplo** | `Ctrl/Cmd + Shift + T` | Open main Triplo window |
| **Quick Prompt** | `Ctrl/Cmd + Shift + P` | Open quick prompt input |
| **Context Mode** | `Ctrl/Cmd + Shift + C` | Show current context |
| **Voice Input** | `Ctrl/Cmd + Shift + V` | Toggle voice input |
| **History** | `Ctrl/Cmd + Shift + H` | Open conversation history |

*Note: Default hotkeys may vary. Check your settings for current assignments.*

## System-Wide Usage Patterns

### Pattern 1: Select → Trigger → Process

**Workflow**:
1. Select text in any application
2. Trigger Triplo with hotkey
3. Triplo automatically uses selected text as context
4. Type your prompt or select a SmartPrompt
5. Get AI response

**Example**:
- Select a long email in Gmail
- Press `Ctrl + Shift + T`
- Type "Summarize this email"
- Get concise summary

### Pattern 2: Window Context → Trigger → Analyze

**Workflow**:
1. Open a document or webpage
2. Trigger Triplo
3. Triplo reads the entire window content
4. Ask questions about the content
5. Get AI analysis

**Example**:
- Open a research paper in PDF viewer
- Press `Ctrl + Shift + T`
- Type "What are the key findings?"
- Get analysis of the paper

### Pattern 3: Clipboard → Trigger → Process

**Workflow**:
1. Copy content to clipboard
2. Trigger Triplo
3. Triplo uses clipboard as context
4. Process with prompt or SmartPrompt
5. Get result

**Example**:
- Copy a support ticket from help desk
- Press `Ctrl + Shift + T`
- Select "Convert to blog post" SmartPrompt
- Get structured blog post content

### Pattern 4: Instant SmartPrompt Execution

**Workflow**:
1. Select content
2. Press assigned SmartPrompt hotkey
3. Triplo executes SmartPrompt immediately
4. Get instant result

**Example**:
- Select code snippet
- Press `Ctrl + Alt + E` (Explain Code)
- Get instant code explanation

## Advanced Triggering

### Context-Aware Triggering

Triplo can be configured to trigger automatically based on context:

**Automatic Triggers** (if enabled):
- Select text → Triplo shows quick actions
- Copy to clipboard → Triplo suggests actions
- Open specific file types → Triplo offers relevant SmartPrompts

**Configuration**:
1. Go to Settings → Automation
2. Enable "Context-Aware Triggers"
3. Configure trigger rules
4. Save settings

### Voice Triggering

**Voice Commands** (desktop):
- "Hey Triplo" + command (if enabled)
- Configure in Settings → Voice

**Mobile Voice**:
- Tap microphone button
- Speak your prompt
- Triplo processes voice input

## Interface Customization

### Theme and Appearance

**Desktop**:
1. Go to Settings → Appearance
2. Choose theme (Light/Dark/System)
3. Adjust font size
4. Customize window behavior (always on top, etc.)

**Mobile**:
1. Go to Settings → Appearance
2. Choose theme
3. Adjust font size
4. Configure notification preferences

### Layout Options

**Desktop**:
- Compact mode: Smaller window, less info
- Expanded mode: More context visible
- Full screen: Maximum workspace

**Mobile**:
- Standard view
- Full screen mode
- Split screen (if supported)

## Troubleshooting UI Issues

### Common Problems

**Issue: Hotkeys not working**
- **Solution**: Check hotkey conflicts with other apps
- **Check**: Triplo settings → Hotkeys
- **Verify**: Triplo has necessary permissions

**Issue: Triplo won't trigger**
- **Solution**: Ensure Triplo is running in background
- **Check**: System tray/menu bar for Triplo icon
- **Verify**: App is not blocked by security software

**Issue: Context not detected**
- **Solution**: Ensure content is selected or window is active
- **Check**: Context panel shows what Triplo sees
- **Verify**: App is supported for context awareness

**Issue: Interface freezes**
- **Solution**: Restart Triplo application
- **Check**: System resources (CPU, memory)
- **Verify**: Latest version installed

## Best Practices

### For Efficiency
- Learn and use hotkeys consistently
- Create instant hotkeys for frequent tasks
- Use context-aware workflows to minimize typing
- Customize interface for your workflow

### For Productivity
- Set up SmartPrompts for repetitive tasks
- Use instant hotkeys for common operations
- Organize SmartPrompts by workflow
- Document your custom hotkeys

### For Learning
- Start with built-in SmartPrompts
- Gradually add custom prompts
- Experiment with different triggering methods
- Find what works best for your workflow

## Next Steps

- **Learn SmartPrompts**: [`smartprompts-and-custom-smartprompts.md`](smartprompts-and-custom-smartprompts.md)
- **Understand Context Awareness**: [`context-awareness-and-sources.md`](context-awareness-and-sources.md)
- **Explore Automations**: [`automations-webhooks-api-magnets.md`](automations-webhooks-api-magnets.md)

---

**Official Documentation**: [documentation.triplo.ai/using-triplo-ai](https://documentation.triplo.ai/using-triplo-ai)
