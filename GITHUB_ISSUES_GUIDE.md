# GitHub Issues & Workflow Guide for AI Agents

**Project**: `Cybersecurity`
**Objective**: Maintain a rigorous, transparent, and up-to-date history of all work, decisions, and progress.

## ⚠️ Prime Directive
**No code changes are committed without a corresponding GitHub Issue.** Taking 30 seconds to track work saves hours of confusion later.

---

## 1. Initialization (Start of Task)

Before writing any code or planning detailed implementation:

1. **Search**: Look for existing issues related to the user's request.
   * *Tool*: `search_issues` (via MCP)
2. **Create (if not found)**: Create a new issue if one does not exist.
   * *Tool*: `issue_write` (via MCP)
3. **Update (if found)**: If an issue exists but is outdated, update it with new context.

### Issue Structure Template
When creating an issue, use this structure:

**Title**: `[Type] Concise Description`
*Types*: `Feature`, `Bug`, `Refactor`, `Docs`, `Chore`

**Body**:
- **Description**: What is the goal?
- **Acceptance Criteria**: 
  - [ ] Criterion 1 (e.g., Page loads without errors)
  - [ ] Criterion 2 (e.g., User can click X)

## Technical Notes
- [Optional: Brief note on implementation strategy, e.g., "Using generic-ui library"]

---

## 2. Execution (During Work)

* **Branching**: specific branches should be created for the issue.
  * **Naming Convention**: `feat/issue-ID-short-description` or `fix/issue-ID-short-description`.
* **Commits**: All commit messages must reference the issue ID.
  * **Format**: `[#ISSUE_ID] Commit message` (e.g., `[#12] Add responsive styles to header`)

---

## 3. Completion (End of Task)

1. **Verification**: Ensure all Acceptance Criteria are met.
2. **Closing**: Close the issue using the GitHub tool.
   * *Tool*: `issue_write` (state: closed)
3. **Comment**: Add a final comment summarizing the resolution if it wasn't a standard PR merge (optional but recommended for complex tasks).

---

## 4. Standard Labels

Apply these labels when creating issues:
* `enhancement`: New features or improvements.
* `bug`: Errors or broken functionality.
* `documentation`: Changes to README, guides, or code comments.
* `refactor`: Code cleanup without logic change.
* `urgent`: Blocks critical workflows.

---

## 5. Agent Instructions (System Prompt Injection)

*When you (the AI Agent) read this file, you must:*
1. Acknowledge that you will track your work.
2. Ask the user for the specific Issue ID if you cannot find one, or ask for permission to create it.
3. Update the issue status as you progress.
