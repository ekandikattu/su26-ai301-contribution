# Contribution [1]: [Add compatibility test for $stdDevPop (second pass)
]

**Contribution Number:** [1]  
**Student:** [Eeshan Kandikattu]  
**Issue:** [[GitHub issue link](https://github.com/documentdb/functional-tests/issues/196)]  
**Status:** [Phase II] [In-Progress]

---

## Why I Chose This Issue

I chose issue #196 "Add compatibility test for $stdDevPop (second pass)" because it aligns with my Python experience and my goal to better implement and understand testing. The issue is labeled "good first issue" and has clear run instructions in the README and clear task instruction in the issue title.

I'm interested in this because I've not delved very deeply into testing and creating testing for specific features/behaviors in my projects. This is something I want to work on and develop through this codebase on an issue meant for first timers.

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

The environment setup seemed straightforward because the README.md was easy to understand and follow for new contributors. I had to install dependencies from the requirements.txt file, but ended up fixing a few things after running the tests.

Tests were missing even though I installed them with `python -m pytest` because I did not have my project `.venv` activated. There was also no database to test against automatically because I would have to set it up. I installed MongoDB Community Server 8.3.4 via `winget install --id MongoDB.Server -e`, which runs as a Windows service on `localhost:27017`.

### Steps to Reproduce

1. Fork and clone the repo, then `cd functional-tests`.
2. Create and activate a virtual environment: `python -m venv .venv` then `.\.venv\Scripts\Activate.ps1 (PowerShell)`. Confirm the prompt shows `(.venv)`.
3. Install dev dependencies: `pip install -r requirements-dev.txt`.
4. Install the contribution prerequisites: `set git config user.name`, add the upstream remote, and run `pre-commit install -t pre-commit -t prepare-commit-msg -t pre-push`.
5. Install a MongoDB instance (I used `winget install --id MongoDB.Server -e`); confirm the service is running and `localhost:27017` is reachable.
6. Run the operator's tests:

`pytest documentdb_tests/compatibility/tests/core/operator/accumulators/stdDevPop/ -v \
  --connection-string mongodb://localhost:27017 --engine-name mongodb`
7. Did not confirm this fully yet! Will do this week.

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

