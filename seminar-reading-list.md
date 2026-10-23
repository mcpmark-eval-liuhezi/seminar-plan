# LLM Agents Reading Seminar — CS594 Course Plan

**Prepared:** 2026-10-23 (department meeting Friday)
**GitHub account used:** HeziLiu (organization: mcpmark-eval-liuhezi)

> **Note on location:** The requested gist could not be created — the GitHub token returns 403 "Resource not accessible by personal access token" on gist creation (no `gist` scope). This plan is therefore stored in this repository under the exact filename `seminar-reading-list.md`. The content is identical to the intended gist.

---

## Reading List (Seminar Order)

1. **Toolformer: Language Models Can Teach Themselves to Use Tools**
   - **arXiv:** 2302.04761
   - **Why:** The canonical self-supervised approach to tool use — the model itself learns which APIs to call, when to call them, and what arguments to pass, so every downstream agent pattern rests on this idea.

2. **ReAct: Synergizing Reasoning and Acting in Language Models**
   - **arXiv:** 2210.03629
   - **Why:** Interleaving reasoning traces with tool actions is the pattern behind virtually every modern agent loop, and its interpretability analysis still sets the seminar agenda.

3. **AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation**
   - **arXiv:** 2308.08155
   - **Why:** The reference framework for multi-agent coordination — customizable, conversable agents mixing LLMs, humans, and tools make it the natural bridge from single-agent tool use to agent teams.

4. **MetaGPT: Meta Programming for a Multi-Agent Collaborative Framework**
   - **arXiv:** 2308.00352
   - **Why:** Shows how encoding human Standardized Operating Procedures into role-based agent societies reduces cascading hallucination — the key "coordination engineering" paper.

*Alternate:* Gorilla: Large Language Model Connected with Massive APIs, arXiv:2305.15334 (tool use; strong API-call reliability/hallucination angle).

---

## Software Shortlist (Agent-Framework Candidates)

From the starred repositories of **HeziLiu** (6 starred total; only one is agent-relevant), plus the leading open-source agent frameworks found on GitHub:

| Repository | Latest release | Notes |
|---|---|---|
| OpenBMB/AgentCPM | *(no GitHub releases/tags)* | Starred on the lab account — end-to-end infrastructure for training & evaluating LLM agents |
| langchain-ai/langchain | langchain-core==1.7.0 (2026-10-22) | Core LLM-application toolkit; tool-calling primitives |
| langchain-ai/langgraph | langgraph==1.2.16 (2026-10-16); CLI langgraph-cli==0.4.37 (2026-10-19) | Graph/state-machine agent orchestration |
| microsoft/autogen | python-v0.7.5 (2025-09-30) | Multi-agent conversation framework (pairs with Reading 3) |
| crewAIInc/crewAI | 1.15.28 (2026-10-14) | Role-based multi-agent "crews" (pairs with Reading 4) |
| openai/openai-agents-python | v0.24.0 (2026-10-15) | Lightweight OpenAI Agents SDK |
| modelcontextprotocol/python-sdk | v2.3.0 | Reference SDK for the Model Context Protocol (tool interop) |

---

## Canvas Course Shell

- **Course name (intended):** LLM Agents Reading Seminar
- **Course code:** CS594

### Intended assignments (seminar order)

1. Reading 1: Toolformer: Language Models Can Teach Themselves to Use Tools
2. Reading 2: ReAct: Synergizing Reasoning and Acting in Language Models
3. Reading 3: AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation
4. Reading 4: MetaGPT: Meta Programming for a Multi-Agent Collaborative Framework

Each: 10 points, online text entry, published, due one week apart starting two weeks from today: **2026-11-06, 2026-11-13, 2026-11-20, 2026-11-27**.

### ⚠️ STATUS: NOT CREATED

Canvas course creation failed. The authenticated user ("MCP Canvas Admin 1", id 34) receives **401 "user not authorized to perform that action"** on every account-level operation (`create_course`, `get_account`, `list_sub_accounts`, `list_account_courses`, `list_account_users`, `get_account_reports`). Only accounts 1 and 2 exist on this instance and both return 401; all other account IDs return 404. The Canvas token in use lacks account/administration permissions.

**No course, assignments, or syllabus exist in Canvas as of 2026-10-23.** The list above is ready to paste into the syllabus once an account-scoped token is available. Note: the assignment tool set has no separate "create page" function; the syllabus body would be set via course update.

---

## GitHub Housekeeping Notes

- **Notifications:** The notifications API is blocked by the token's scopes (403 "Resource not accessible by personal access token" on both listing and marking read). Nothing could be read or marked read. As a closest proxy, searches for open issues/PRs assigned to or mentioning HeziLiu were run — see flagged items in the chat summary. **The inbox itself remains untouched.**
- **Teams:** HeziLiu belongs to org **mcpmark-eval-liuhezi** but is on **zero teams**. There are no team members to approach as a co-grader via GitHub. A co-grader will need to come from outside the org, or an org admin would need to add the account to a team first.

---

*Prepared with live API verification of papers (arXiv), releases (GitHub), and permissions (Canvas + GitHub). Search-based arXiv discovery was persistently rate-limited (HTTP 429); the four papers above were individually downloaded and verified from arXiv instead.*
