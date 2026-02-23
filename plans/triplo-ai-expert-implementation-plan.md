# Triplo AI Expert Skill Implementation Plan

## Overview

This plan outlines the creation of a specialized "Triplo AI Expert" agent skill designed to guide users through the Triplo AI ecosystem. The skill follows the skill-creator standard of concise SKILL.md routing and detailed references/.

## Project Structure

```
triplo-ai-expert/
├── SKILL.md                              # Main entry point with YAML frontmatter
├── references/                           # Domain-specific reference files
│   ├── overview-and-personas.md
│   ├── getting-started-install-activate.md
│   ├── ui-triggering-and-hotkeys.md
│   ├── smartprompts-and-custom-smartprompts.md
│   ├── context-awareness-and-sources.md
│   ├── training-and-knowledge-bases.md
│   ├── automations-webhooks-api-magnets.md
│   ├── chat-mode-voice-and-conversation.md
│   ├── agents-and-connections.md
│   ├── models-allowances-and-byok.md
│   ├── openrouter-models-strengths.md
│   ├── local-models-strengths.md
│   ├── local-llms-setup-desktop-mobile.md
│   ├── security-privacy-and-data.md
│   ├── troubleshooting-and-faq.md
│   └── learning-paths-and-resources.md
├── scripts/                             # Optional helper scripts
│   └── scenario_templates.md
└── assets/                              # Prompt templates and checklists
    └── prompt-templates-and-checklists/
```

## Implementation Phases

### Phase 1: Core Structure (SKILL.md)

**Objective**: Create the main SKILL.md file with proper YAML frontmatter and progressive disclosure routing.

**Key Components**:
- YAML frontmatter with name, description, and metadata
- "How to use this skill" section for the agent
- Progressive disclosure links to reference files
- Behavioral mode definitions (Advisor, Coach, Builder, Troubleshooter)
- Strategy for staying current with docs

**Constraints**:
- Keep SKILL.md under 500 lines
- No long tutorials - route to references instead
- Clear behavioral mode instructions

### Phase 2: Reference Files Creation

**Objective**: Create 16 specialized reference files mapping to Triplo AI knowledge domains.

**Reference File Specifications**:

1. **overview-and-personas.md**
   - What Triplo AI is
   - Key differentiators (system-wide assistant, no integrations, multi-platform)
   - User personas (knowledge workers, creators, researchers)

2. **getting-started-install-activate.md**
   - Installation on supported platforms
   - Activation and device/key association
   - Subscription & refunds
   - Device management
   - Customizing model list per device

3. **ui-triggering-and-hotkeys.md**
   - Triggering Triplo UI from anywhere
   - Main interfaces
   - Hotkeys for instant prompt execution
   - System-wide usage patterns

4. **smartprompts-and-custom-smartprompts.md**
   - Using built-in SmartPrompts
   - Creating Custom SmartPrompts
   - Encoding instructions for consistent AI behavior

5. **context-awareness-and-sources.md**
   - Awareness features (Context/Selection/Clipboard)
   - Using files and images
   - Scraping web pages and YouTube subtitles
   - Using desktop/mobile content as context

6. **training-and-knowledge-bases.md**
   - Training/Minds/Knowledge Bases concept
   - Building multiple trusted knowledge bases
   - Feeding generation for trustworthy outputs

7. **automations-webhooks-api-magnets.md**
   - Automations via webhooks and API calls
   - Magnets (snapping models, instructions, Minds, automations)
   - Example automation scenarios

8. **chat-mode-voice-and-conversation.md**
   - Chat Mode vs single-shot prompts
   - Voice interaction (speaking & listening)
   - Conversational workflow guidance

9. **agents-and-connections.md**
   - Agents [BETA] concept & usage
   - OpenAI-compatible Connections
   - When to use external endpoints vs native models

10. **models-allowances-and-byok.md**
    - Included models
    - Monthly token allowances (2M tokens per device)
    - BYOK via OpenAI/OpenRouter
    - Model selection guidance by use case

11. **openrouter-models-strengths.md**
    - Summaries of "Open Router Models and its Strengths"
    - Note: Must be re-read for model-comparison questions (date-stamped)

12. **local-models-strengths.md**
    - Summaries of "Local Models and its Strengths"
    - When to use local vs hosted models
    - Setup considerations

13. **local-llms-setup-desktop-mobile.md**
    - Setting up local LLMs on desktop
    - Accessing local models on mobile
    - How Triplo routes traffic to local models

14. **security-privacy-and-data.md**
    - Triplo's data handling approach
    - Local history/log storage locations
    - Relevant parts of "How Triplo AI deal with Data"

15. **troubleshooting-and-faq.md**
    - Consolidated patterns from FAQ and docs
    - Activation issues
    - Device limit problems
    - SmartPrompts not behaving as expected
    - Training not affecting outputs
    - Token limit errors

16. **learning-paths-and-resources.md**
    - Curated learning tracks (Beginner → Power User)
    - Pointing to specific doc sections
    - YouTube content recommendations
    - Agent prompts to guide users

**Reference File Standards**:
- Concise content with links to canonical docs
- Progressive disclosure structure
- Links/anchors back to official documentation pages
- No duplication of long text from docs

### Phase 3: Supporting Assets

**scripts/scenario_templates.md**
- Scenario templates for common workflows
- Optional update-check helpers

**assets/prompt-templates-and-checklists/**
- Ready-to-use prompt templates
- Checklists for common tasks
- Best practice guides

### Phase 4: Validation & Testing

**Automated Validation**:
- Validate SKILL.md frontmatter with package_skill.py
- Ensure all relative links resolve to references/ directory

**Manual Review**:
- Review SKILL.md length (<500 lines)
- Verify behavioral modes are clearly defined
- Check progressive disclosure routing
- Confirm all reference files exist and are properly linked

### Phase 5: Publishing

**Local Staging**:
- Build files in `C:\Users\bradb\.agent\skills\triplo-ai-expert`

**Repository Sync**:
- Copy triplo-ai-expert folder to `C:\Users\bradb\Activepieces\my-agent-skills\`

**Repository Update**:
- Add triplo-ai-expert to root README.md
- Update installation command example

**Push to GitHub**:
- Execute git add, commit, and push to tparrin/my-agent-skills

## Behavioral Modes

The skill must support four distinct interaction modes:

### 1. Advisor / Explainer
- **Trigger**: User asks "What is Triplo / SmartPrompts / Training / Agents?"
- **Behavior**: Provide high-level concepts, use cases, and trade-offs
- **References**: overview, feature descriptions, relevant docs

### 2. Coach / Trainer
- **Trigger**: User wants to learn
- **Behavior**: Provide stepwise walkthroughs ("do X in the UI, then Y")
- **References**: installation, UI/triggering, feature docs
- **Includes**: Practice exercises (e.g., "Let's design 3 SmartPrompts")

### 3. Builder / Co-creator
- **Trigger**: User wants prompts, automations, knowledge-base designs
- **Behavior**: Help draft SmartPrompts, Training plans, webhook payloads, model-selection strategies
- **References**: automations, training, model strengths docs

### 4. Troubleshooter
- **Trigger**: Something "doesn't work"
- **Behavior**: Guide through canonical troubleshooting playbook
- **Checks**: Activation status, device limits, Training coverage, wrong model selection, token limits, outdated docs
- **References**: FAQ, changelog

### 5. Meta-advisor about Learning Resources
- **Trigger**: User needs deeper learning
- **Behavior**: Recommend relevant doc sections, Triplo resources, video content
- **References**: SmartPrompts library, Changelog, YouTube

## Staying Current Strategy

The skill must explicitly instruct the agent to:

**Re-read frequently updated docs** for:
- Available models and their strengths (OpenRouter and local models)
- New features and UI changes (changelog and roadmap)

**Prefer references over memory** for:
- Security, privacy, allowances, local history/log storage
- Consult relevant sections of documentation.triplo.ai

**Surface "check latest source" when**:
- Answering version- or pricing-sensitive questions
- Exact values may have changed
- User should confirm via official docs or support

## Source Documentation

**Primary Sources**:
- Main marketing site: `triplo.ai/en`
- Documentation hub: `documentation.triplo.ai`
- Triplo AI YouTube channel

**Frequently Updated Sections**:
- "Open Router Models and its Strengths" (dated updates)
- "Local Models and its Strengths" (dated updates)
- Feature changelog
- Roadmap/support sections

## Success Criteria

1. ✅ SKILL.md is under 500 lines with clear routing
2. ✅ All 16 reference files created with proper content
3. ✅ All relative links resolve correctly
4. ✅ Behavioral modes are clearly defined and actionable
5. ✅ Frontmatter validates with package_skill.py
6. ✅ Repository README.md updated with installation command
7. ✅ Skill successfully pushed to GitHub
8. ✅ Manual review confirms quality and completeness

## Next Steps

1. Review and approve this plan
2. Switch to Code mode for implementation
3. Execute tasks in the defined order
4. Validate and test at each phase
5. Publish to repository upon completion

---

**Note**: This implementation plan is based on the Triplo AI_Research.md document and follows the Skill Creator best practices for skills.sh compatibility.
