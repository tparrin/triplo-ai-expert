# Chat Mode, Voice, and Conversation

## Chat Mode vs. Single-Shot Prompts

Triplo AI supports two main interaction modes:

### Single-Shot Prompts

**What it is**: One question, one answer. Each prompt is independent.

**When to use**:
- Quick questions
- One-off tasks
- Simple requests
- Testing ideas

**Example**:
- "Summarize this email"
- "Rewrite this paragraph"
- "What does this code do?"

**Benefits**:
- Fast and efficient
- No context carryover
- Clear boundaries
- Easy to manage

### Chat Mode

**What it is**: Conversational interaction with context maintained across multiple turns.

**When to use**:
- Complex tasks requiring multiple steps
- Iterative refinement
- Exploring topics in depth
- Building on previous responses

**Example**:
```
User: "What are the key features of this product?"
AI: [Lists features]
User: "Tell me more about feature X"
AI: [Explains feature X]
User: "How does it compare to competitors?"
AI: [Provides comparison]
```

**Benefits**:
- Maintains context
- Enables exploration
- Builds understanding
- More natural interaction

## Using Chat Mode

### Starting a Chat

**How to enter Chat Mode**:
1. Trigger Triplo AI
2. Select "Chat Mode" from interface
3. Start conversing

**Visual indicators**:
- Chat interface shows conversation history
- Context panel shows accumulated context
- Each message is timestamped

### Chat Mode Features

**Context retention**:
- Triplo remembers previous messages
- References earlier parts of conversation
- Maintains topic continuity

**Multi-turn conversations**:
- Ask follow-up questions
- Request clarifications
- Explore related topics
- Refine responses

**Context management**:
- See what Triplo remembers
- Add or remove context
- Reset conversation if needed
- Branch conversations (if supported)

### Chat Mode Workflows

**Workflow 1: Iterative Analysis**
```
1. User: "Analyze this document"
2. AI: [Provides initial analysis]
3. User: "Focus on the financial section"
4. AI: [Dives deeper into financials]
5. User: "What are the risks?"
6. AI: [Identifies risks]
```

**Workflow 2: Content Creation**
```
1. User: "Draft a blog post about X"
2. AI: [Provides draft]
3. User: "Make it more professional"
4. AI: [Refines tone]
5. User: "Add a call to action"
6. AI: [Adds CTA]
7. User: "Shorten the intro"
8. AI: [Condenses intro]
```

**Workflow 3: Problem Solving**
```
1. User: "I'm getting this error: [error message]"
2. AI: [Suggests solutions]
3. User: "I tried solution 1, didn't work"
4. AI: [Offers alternative]
5. User: "Here's more context: [details]"
6. AI: [Refines diagnosis]
```

## Voice Interaction

### Speaking to Triplo

**Voice Input (Desktop)**:
1. Trigger Triplo AI
2. Click microphone icon or press voice hotkey
3. Speak your prompt
4. Triplo transcribes and processes
5. Get text response (or voice response if enabled)

**Voice Input (Mobile)**:
1. Open Triplo app
2. Tap microphone button
3. Speak your prompt
4. Triplo transcribes and processes
5. Get response

### Voice Output (Text-to-Speech)

**Hearing Triplo's Response**:
1. Enable voice output in settings
2. When Triplo responds, it speaks the answer
3. Adjust voice settings (speed, pitch, etc.)
4. Choose from available voices

**When voice output is useful**:
- Hands-free operation
- Accessibility needs
- Learning pronunciation
- Multitasking

### Voice Settings

**Configuration options**:
- **Voice selection**: Choose from available voices
- **Speed**: Adjust speaking rate
- **Pitch**: Modify voice pitch
- **Volume**: Control output volume
- **Language**: Set language preference

**Best practices**:
- Test different voices for clarity
- Adjust speed for comprehension
- Use appropriate voice for context
- Consider environment (quiet vs. noisy)

## Conversation Patterns

### Pattern 1: Exploratory Conversations

**Purpose**: Learn about a topic deeply.

**Structure**:
1. Start with broad question
2. Follow up on interesting points
3. Ask for examples
4. Request clarifications
5. Explore related topics

**Example**:
```
User: "Explain machine learning"
AI: [Explains ML]
User: "What's the difference between supervised and unsupervised?"
AI: [Explains difference]
User: "Give me an example of each"
AI: [Provides examples]
User: "Which is better for my use case?"
AI: [Analyzes use case]
```

### Pattern 2: Refinement Conversations

**Purpose**: Improve or refine output iteratively.

**Structure**:
1. Request initial output
2. Provide feedback
3. Request changes
4. Iterate until satisfied

**Example**:
```
User: "Write an email about the product launch"
AI: [Drafts email]
User: "Make it more exciting"
AI: [Adds enthusiasm]
User: "Shorten it to 3 paragraphs"
AI: [Condenses]
User: "Add a call to action"
AI: [Adds CTA]
```

### Pattern 3: Diagnostic Conversations

**Purpose**: Solve problems through dialogue.

**Structure**:
1. Describe problem
2. AI asks clarifying questions
3. Provide details
4. AI suggests solutions
5. Test and report back

**Example**:
```
User: "My code isn't working"
AI: "What error are you getting?"
User: [Provides error]
AI: "What does the code do?"
User: [Explains purpose]
AI: [Suggests fix]
User: "That worked! But now I have another issue"
AI: "What's the new issue?"
```

## Advanced Conversation Techniques

### 1. Context Switching

**When to switch**: Moving to a new topic mid-conversation.

**How to do it**:
- Explicitly state topic change
- "Let's talk about something else"
- "Switching topics now"
- "New question:"

**Example**:
```
User: "How do I optimize this query?"
AI: [Explains optimization]
User: "Okay, let's switch topics. How do I secure the database?"
AI: [Shifts to security topic]
```

### 2. Branching Conversations

**When to branch**: Exploring different directions from the same starting point.

**How to do it**:
- Save current conversation state
- Start new branch
- Explore alternative
- Compare results

**Example**:
```
User: "Write a marketing email"
AI: [Drafts email A]
User: "Save this. Now write another version"
AI: [Drafts email B]
User: "Compare the two"
AI: [Analyzes differences]
```

### 3. Role-Based Conversations

**When to use**: Need specific expertise or perspective.

**How to do it**:
- Define role at start
- "Act as a [role]"
- "You are a [expert type]"
- Maintain role throughout

**Example**:
```
User: "Act as a marketing expert. Review this ad copy"
AI: [Provides expert analysis]
User: "What would you change?"
AI: [Suggests improvements from expert perspective]
```

### 4. Multi-Modal Conversations

**When to use**: Combining text, voice, and visual context.

**How to do it**:
- Select text or upload file
- Use voice for prompts
- Reference visual content
- Combine all modes

**Example**:
```
User: [Selects chart in spreadsheet]
User: [Speaks] "What does this chart show?"
AI: [Analyzes chart and explains]
User: [Speaks] "What are the trends?"
AI: [Identifies trends]
```

## Best Practices

### For Effective Chat Mode

1. **Be clear about context**
   - State what you're working on
   - Reference previous messages
   - Explicitly switch topics

2. **Provide feedback**
   - Tell Triplo if response is good or bad
   - Specify what to improve
   - Guide the conversation

3. **Use follow-up questions**
   - Don't try to get everything in one question
   - Build understanding gradually
   - Explore related topics

4. **Manage conversation length**
   - Reset if conversation gets too long
   - Start new conversation for new topics
   - Archive useful conversations

### For Voice Interaction

1. **Speak clearly**
   - Enunciate words
   - Use natural pace
   - Minimize background noise

2. **Use concise prompts**
   - Voice input is slower than typing
   - Keep prompts focused
   - Avoid long monologues

3. **Test voice settings**
   - Adjust speed for comprehension
   - Choose clear voices
   - Test in your environment

4. **Use voice when appropriate**
   - Hands-free situations
   - Accessibility needs
   - When typing is inconvenient

### For Conversation Management

1. **Organize conversations**
   - Use descriptive names
   - Archive important conversations
   - Delete unnecessary ones

2. **Review history**
   - Learn from past conversations
   - Find useful patterns
   - Reference previous insights

3. **Reset when needed**
   - Don't let conversations get too long
   - Start fresh for new topics
   - Clear context if confused

## Troubleshooting

### Common Issues

**Issue: Triplo forgets context**
- **Solution**: Check context panel, explicitly reference earlier messages
- **Verify**: Conversation hasn't been reset

**Issue: Voice not working**
- **Solution**: Check microphone permissions, test audio input
- **Verify**: Voice settings are enabled

**Issue: Voice output not playing**
- **Solution**: Check volume, verify voice output is enabled
- **Test**: Different voice settings

**Issue: Conversation is confusing**
- **Solution**: Reset conversation, start fresh with clear context
- **Check**: Topic switches are explicit

## Next Steps

- **Learn about Agents**: [`agents-and-connections.md`](agents-and-connections.md)
- **Explore Models**: [`models-allowances-and-byok.md`](models-allowances-and-byok.md)
- **Understand Automations**: [`automations-webhooks-api-magnets.md`](automations-webhooks-api-magnets.md)

---

**Official Documentation**: [documentation.triplo.ai/using-triplo-ai/chat-mode](https://documentation.triplo.ai/using-triplo-ai/chat-mode)
