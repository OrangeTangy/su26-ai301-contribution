# Contribution 1: Control API for AI-assisted comment resolution

**Contribution Number:** 1  
**Student:** Tanay Anand 
**Issue:** [mavaali/tippani #42](https://github.com/mavaali/tippani/issues/42)  
**Status:** Phase I — Complete

---

## Why I Chose This Issue

**The issue.** [tippani](https://github.com/mavaali/tippani) is a CLI that renders Azure DevOps pull-request markdown as a clean three-column review portal, but resolving review comments is entirely manual — you read a thread, type a reply, click resolve, and scroll to the next one. Issue #42 proposes a lightweight HTTP + Server-Sent-Events "control API" that lets an external tool (an LLM assistant, a script, or an IDE extension) drive tippani's UI — list comment threads, scroll to and highlight a thread, and stage a draft reply — while the human reviewer keeps final approval in the browser. It matters because it turns tippani into a shared visual layer between a reviewer and an AI assistant, cutting a 15-thread review from roughly 15 minutes to 3, without ever auto-posting on the user's behalf.

**Why I chose it.** It's an uncontested `good first issue` / `P1` on an actively maintained repo, and it's plain Node/Express/JavaScript I can ramp on quickly. Most importantly the scope is bounded and buildable in slices: much of the proposal *extends* an existing server rather than starting from scratch — `/api/reply` and `/api/resolve` already exist, thread data is already serialized to the client, and the scroll-to-thread-and-highlight behavior is already implemented — so the genuinely new work (a `GET /sse` event channel, a draft-staging UI, and a few read-only endpoints) is something I can land as a reviewable MVP first and then extend. The AI-assisted-review angle also lines up with my interest in developer tooling.

---

## Understanding the Issue

### Problem Description

[In your own words, what's broken or missing?]

### Expected Behavior

[What should happen?]

### Current Behavior

[What actually happens?]

### Affected Components

[Which parts of the codebase are involved?]

---

## Reproduction Process

### Environment Setup

[Notes on setting up your local development environment - challenges you faced, how you solved them]

### Steps to Reproduce

1. [Step 1]
2. [Step 2]
3. [Observed result]

### Reproduction Evidence

- **Commit showing reproduction:** [Link to commit in your fork]
- **Screenshots/logs:** [If applicable]
- **My findings:** [What you discovered during reproduction]

---

## Solution Approach

### Analysis

[Your analysis of the root cause - what's causing the issue?]

### Proposed Solution

[High-level description of your fix approach]

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** [Restate the problem]

**Match:** [What similar patterns/solutions exist in the codebase?]

**Plan:** [Step-by-step implementation plan]
1. [Modify file X to do Y]
2. [Add function Z]
3. [Update tests]

**Implement:** [Link to your branch/commits as you work]

**Review:** [Self-review checklist - does it follow the project's contribution guidelines?]

**Evaluate:** [How will you verify it works?]

---

## Testing Strategy

### Unit Tests

- [ ] Test case 1: [Description]
- [ ] Test case 2: [Description]
- [ ] Test case 3: [Description]

### Integration Tests

- [ ] Integration scenario 1
- [ ] Integration scenario 2

### Manual Testing

[What you tested manually and results]

---

## Implementation Notes

### Week [X] Progress

[What you built this week, challenges faced, decisions made]

### Week [Y] Progress

[Continue documenting as you work]

### Code Changes

- **Files modified:** [List]
- **Key commits:** [Links to important commits]
- **Approach decisions:** [Why you chose certain approaches]

---

## Pull Request

**PR Link:** [GitHub PR URL when submitted]

**PR Description:** [Draft or final PR description - much of the content above can be adapted]

**Maintainer Feedback:**
- [Date]: [Summary of feedback received]
- [Date]: [How you addressed it]

**Status:** [Awaiting review / Iterating / Approved / Merged]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]

### Challenges Overcome

[What was hard and how you solved it]

### What I'd Do Differently Next Time

[Reflection on your process]

---

## Resources Used

- [Link to helpful documentation]
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]
