# AGENTS.md

## Purpose

This file provides **guidelines for automation agents** (such as Copilot, Codex, or other LLM-powered assistants) contributing to the `awesome-netsuite-ai` repository.
It defines **expected workflows**, **common pitfalls**, and **rules of engagement** to ensure consistent, high-quality contributions.

---

## Core Responsibilities

Agents are expected to:

1. Maintain the integrity of the [Awesome List guidelines](https://github.com/sindresorhus/awesome).
2. Follow project-specific conventions for content structure, formatting, and attribution.
3. Run linting and tests before finalising changes.
4. Add value — every addition must be relevant to **NetSuite AI**, **MCP (Model Context Protocol)**, or the **AI Connector Service**.

---

## Contribution Workflows

### Adding New Entries

* **Verify links**: Ensure the URL works and is not gated.
* **Choose correct section**:

  * 🏢 Official Resources
  * 📚 Articles & Guides
  * 🛠️ Sample Code & Tools
  * 🎥 Videos & Tutorials
  * 💡 Use Cases & Examples
  * 👥 Community
* **Formatting**:

  * `[Title](url) - Description by Author Name.`
  * End descriptions with a period.
  * Include author attribution for all articles, guides, and videos.
* **Ordering**: Alphabetical within each section.
* **Lint check**: Run `npm run lint` before committing.

### Modifying README

* **TOC Compliance**:

  * Heading must be `## Contents`.
  * TOC links must include emojis, but anchors strip them.
  * Example: `[🎥 Videos & Tutorials](#-videos--tutorials)` → `## 🎥 Videos & Tutorials`.
* **Spacing**:

  * Keep a blank line before and after sections.
  * Maintain consistent indentation for list items.
* **Commit messages**: Use `docs:` prefix for content additions or updates.
  Example: `docs: add async saved search guide`.

### Testing & Validation

* Run:

  ```bash
  npm run lint
  npm test
  ```
* Lint checks include:

  * TOC accuracy.
  * Valid GitHub repository recognition (must have a valid remote).
  * Description and ordering compliance.

---

## Integration Notes

### Automation Tools

* **awesome-lint**: Enforces awesome list rules.
* **GitHub Actions**: Runs linting on all PRs and pushes.
* **Node.js 18+**: Ensure environment consistency.

### Repository Setup

* Git remote must point to a valid GitHub repository, or lint will fail with:

  ```
  ✖ 1:1 Awesome list must reside in a valid git repository
  ```
* Common workaround during local/dev runs:

  ```bash
  git remote add origin https://github.com/<user>/<repo>.git
  ```

---

## Common Pitfalls

* **Lint Failures**:

  * Missing or mis-formatted TOC entries.
  * Emoji mismatch between TOC and headings.
  * Repo not linked to GitHub (invalid remote).
* **Description issues**:

  * Missing author name.
  * Missing final period.
* **Ordering mistakes**:

  * Items not alphabetised.
  * Items placed in the wrong section.
* **Long logs**: Use `CI=true npm test` or pipe through `tr '\r' '\n'` to avoid spinner overflow.

---

## Examples

### Correct Video Entry

```markdown
- [NetSuite AI Connector Walkthrough](https://www.linkedin.com/posts/james-sarhan-02332616b_netsuite-oracle-ai-activity-7364346164860657664-fH1Z/) - James Sarhan showcases Oracle's NetSuite AI Connector, demonstrating how Claude integrates with NetSuite to retrieve data with natural language and automate tasks.
```

### Correct Guide Entry

```markdown
- [Async Saved Searches via NetSuite MCP Custom Tool](https://www.linkedin.com/posts/tanwasripan_netsuite-ai-mcp-activity-7370512683097296896-V8BL) - Tanwa Sripan demonstrates using the N/task module to run saved searches asynchronously when the N/search module is not supported.
```

---

## Final Checklist for Agents

Before committing, confirm:

* [ ] Link is valid and relevant.
* [ ] Correct section chosen.
* [ ] Alphabetical placement verified.
* [ ] Author attribution present.
* [ ] Description ends with a period.
* [ ] `npm run lint` passes without errors.
* [ ] Commit message follows convention.

---

✅ With these rules, agents will contribute consistently and maintain the high quality of this Awesome List.