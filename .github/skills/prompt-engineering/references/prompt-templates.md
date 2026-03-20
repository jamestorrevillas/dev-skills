# Prompt Templates Reference

Ready-to-use prompt templates for common developer tasks.

---

## Code Generation

### Feature Implementation
```
You are a senior [language] developer.
Implement [feature description].

Requirements:
- [requirement 1]
- [requirement 2]

Constraints:
- [stack/framework constraints]
- [style/pattern constraints]

Before writing code, outline your approach in 3-5 bullet points.
Then implement it. After writing, verify edge cases are handled.
```

### Code Refactoring
```
You are a senior software engineer focused on clean code.
Refactor the following code to improve [readability/performance/maintainability].

Rules:
- Preserve all existing behavior (no functional changes)
- Follow [SOLID / DRY / existing patterns in the codebase]
- Do NOT add new dependencies

Code:
"""
[paste code]
"""

Explain each change and why it improves the code.
```

### Bug Fix
```
You are a debugging expert.
The following code has a bug: [describe symptom]

Expected behavior: [what should happen]
Actual behavior: [what is happening]

Code:
"""
[paste code]
"""

Step 1: Identify the root cause (not just the symptom)
Step 2: Propose the fix
Step 3: Verify the fix doesn't introduce new issues
Step 4: Suggest a test that would catch this bug in the future
```

---

## Code Review

### Security Review
```
You are a security engineer specializing in OWASP Top 10.
Review this code for security vulnerabilities.

For each issue found, provide:
- Severity: CRITICAL / HIGH / MEDIUM / LOW
- Description of the vulnerability
- Specific fix with code example
- CWE reference if applicable

Code:
"""
[paste code]
"""
```

### Architecture Review
```
You are a staff engineer reviewing a pull request.
Evaluate this code change from an architectural perspective.

Tag each comment as: BLOCKER / WARNING / SUGGESTION / PRAISE

Consider:
- Does it follow existing patterns?
- Is it testable?
- Will it scale?
- Is the abstraction level correct?

Code:
"""
[paste code]
"""
```

---

## Documentation

### README Generation
```
You are a technical writer.
Generate a README.md for this project.

Project purpose: [describe what it does]
Target audience: [developers / end users / both]

Include these sections:
- Overview (2-3 sentences)
- Prerequisites
- Installation
- Usage with examples
- Configuration
- Contributing guidelines

Keep it concise. Prefer examples over lengthy explanations.
```

### Function Documentation
```
Write clear documentation for this function.

Format: JSDoc / Python docstring / [your format]

Include:
- One-line description
- Parameter descriptions with types
- Return value description
- Example usage
- Any important side effects or exceptions

Function:
"""
[paste function]
"""
```

---

## Architecture & Design

### System Design
```
You are a solutions architect.
Design a system for: [describe the problem]

Scale requirements: [users, requests/sec, data volume]
Constraints: [budget, existing stack, team size]

Provide:
1. High-level architecture diagram (as text/ASCII)
2. Component breakdown with responsibilities
3. Data flow description
4. Key technical decisions with trade-offs
5. What you explicitly chose NOT to include and why
```

### API Design
```
You are an API design expert.
Design a [REST / GraphQL / tRPC] API for: [describe the domain]

Requirements:
- [functional requirement 1]
- [functional requirement 2]

Provide:
- Endpoint definitions with HTTP methods and paths
- Request/response schemas
- Error handling strategy
- Authentication approach
- Versioning strategy
```

---

## Testing

### Test Generation
```
You are a QA engineer who writes thorough tests.
Write [Jest/pytest/JUnit] tests for this function.

Cover:
1. Happy path (expected inputs)
2. Edge cases (null, empty, boundary values)
3. Error paths (invalid inputs, exceptions)

Use AAA pattern (Arrange / Act / Assert).
Each test should test ONE behavior.
Mock all external dependencies.

Function:
"""
[paste function]
"""
```

### E2E Test Generation
```
You are a Playwright testing expert.
Write an E2E test for this user flow: [describe flow]

Requirements:
- Use getByRole() and getByLabel() selectors (not CSS classes)
- Include assertions for each major state
- Handle async operations with proper waits
- Add a descriptive test name

Base URL: [your app URL]
```

---

## Learning & Explanation

### Explain Concept
```
You are a patient senior developer teaching a junior.
Explain [concept] at the level of someone who knows [prior knowledge level].

Structure:
1. One-sentence definition
2. Why it matters (practical use case)
3. Simple example
4. Common mistake to avoid
5. "Learn more" pointer to official docs
```

### Socratic Learning Mode
```
I want to learn [topic/concept] through dialogue, NOT just receive answers.

Rules:
- Do NOT give me the solution directly
- Ask me questions to guide my thinking
- Point out what I'm missing without filling it in
- Challenge my assumptions
- Only confirm when my reasoning is correct

My current understanding: [describe what you know]
My question: [what you want to understand]
```

---

## Planning & Spec Writing

### Feature Spec
```
You are a tech lead writing a feature specification.
Write a spec for: [feature description]

Sections:
1. Problem Statement (what problem does this solve?)
2. Goals (what success looks like)
3. Non-Goals (what this explicitly does NOT cover)
4. Proposed Solution (high-level approach)
5. Technical Design (components, data models, APIs)
6. Open Questions (decisions still needed)
7. Definition of Done (acceptance criteria)
```

### Task Breakdown
```
Break this feature into implementable tasks for a sprint.

Feature: [description]
Team size: [n developers]
Sprint length: [n days]

For each task:
- Title (action-oriented)
- Story points (1/3/5/8/13)
- Dependencies (which tasks must come first)
- Acceptance criteria (1-3 bullet points)

Order tasks so earlier ones unblock later ones.
Flag any tasks with uncertainty that need more discussion.
```
