# Agent Operating Guidelines

## Context management

When you need additional information to make decisions:

1. **Ask specifically** - "I need the user research data on how people currently handle X"
2. **State why** - "This will help me design the error handling for scenario Y"  
3. **Request by document** - Ask for specific files by name when they exist

Available supporting documents:

- <technical-guidelines.md>
- <design-requirements.md>  
- <decision-log.md>

Don't assume - if you're unsure about requirements, user behavior, or technical constraints, ask for the relevant context.

## Development philosophy

- Simple, Lovable, Complete (SLC) over traditional MVP
- Ship features that feel finished rather than half-built
- Better to do fewer things well than many things poorly
- Each feature should delight users, not just technically function

Simply, Lovable, Complete prioritizes user experience and emotional connection over speed. This approach, popularized by companies like Linear, means we will take more time upfront to create something users genuinely enjoy using, even in its first iteration. The product feels polished and thoughtfully designed rather than hastily assembled.

## Making decisions

Defintitions: 

[Human-Decides] - Human makes the call, agent implements
[Agent-Proposes-Human-Decides] - Agent suggests options, human chooses
[Agent-Decides-Human-Review] - Agent decides and implements, human can override
[Agent-Decides] - Agent has full authority, no review needed
[Collaborative] - Both parties discuss until consensus reached
[Already-Decided] - Pre-established in project docs

Decision Types: 

- Architecture decisions: [Agent-Decides-Human-Review]
- UX decisions: [Agent-Proposes-Human-Decides]
- Implementation details: [Agent-Decides]
- Scope changes: [Human-Decides]
- Technology choices: [Collaborative]

## Code quality

- Use TypeScript strict mode, avoid `any` when possible
- Follow existing project patterns for consistency
- Include error handling for all external API calls
- Write self-documenting code with clear variable names
