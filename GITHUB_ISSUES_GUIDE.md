# GitHub Issues & Milestones Tracking Guide for AI Agents

Welcome! As an AI agent working on this repository, one of your core responsibilities is maintaining strict discipline over project management using GitHub Issues and Milestones. Before and after any development work, you must ensure our progress is accurately reflected in GitHub.

**Repository Context:** `ramtirthjoshi-boop/Cybersecurity`

## 1. Core Principles
- **No Orphaned Work:** Every pull request, code change, or major research task MUST be tied to an active GitHub Issue.
- **Proactive Management:** You are responsible for creating, updating, and closing issues autonomously based on the user's requests.
- **Milestone Alignment:** All issues should belong to an active Milestone to track high-level project goals.

## 2. Issue Management Protocol

### Creating New Issues
Whenever a new feature, bug fix, or task is identified that doesn't have an existing issue:
1. **Title:** Use clear, descriptive titles (e.g., `[Feature] Implement User Authentication`, `[Bug] Fix crash on login`).
2. **Body:** 
   - Provide a brief summary of the problem or feature.
   - List acceptance criteria (checkboxes are preferred: `- [ ] Criterion`).
   - Mention any related files or context.
3. **Labels:** Apply relevant labels (`enhancement`, `bug`, `documentation`, `in-progress`).
4. **Milestone:** Assign the issue to the current active milestone.

### Updating Existing Issues
As work progresses:
1. **Status Comments:** Add brief comments to the issue summarizing major steps completed.
2. **Task Lists:** Check off completed tasks in the issue body.
3. **Labeling:** Update labels if the scope changes (e.g., adding `blocked` if waiting on a dependency).

### Closing Issues
When work is fully verified and pushed to the default branch:
1. Ensure all acceptance criteria are met.
2. Close the issue with a comment referencing the commit or summarizing the resolution.

## 3. Workflow Triggers

**Before writing code:**
- Search for existing issues using the GitHub MCP tool (`list_issues` or `search_issues`).
- If an issue exists, assign yourself (if possible) or add a comment stating work has begun.
- If no issue exists, create one immediately using `issue_write`.

**During development:**
- If the scope expands significantly, create sub-issues or update the parent issue description.

**After writing code (Before concluding your turn):**
- Update the relevant issue's status.
- Ensure milestones reflect the completed work.

## 4. MCP Tools Reference
Utilize the following GitHub MCP tools to execute these rules:
- `search_issues` / `list_issues`: Check existing tasks.
- `issue_write`: Create new issues or update descriptions/labels/milestones.
- `add_issue_comment`: Leave status updates.

> **Note to AI:** By reading this file, you acknowledge that project tracking is just as critical as the code itself. Stay disciplined!
