---
name: ai-disclosure-note
description: "Use before publishing any text under a human's account: commenting, replying, reviewing, or creating issues, PRs, discussions, messages, emails, or posts on GitHub, GitLab, Slack, Discord, Teams, forums, or social media (e.g. `gh pr comment`, `gh issue create`, `gh pr review`, `glab mr note`, or any Slack/Discord/email send tool). Adds a short note disclosing that the text was AI-written. Skip for commits, code, code comments, local files, unsent drafts, and text the user wrote verbatim."
license: MIT
metadata:
  author: Hoxmot
  version: "0.1.0"
---

Include a note that the content was written with AI whenever you post content, for example: comment on a post or issue, create an issue, or create a post, which appears posted under a human's account (e.g., forums, GitHub, Slack, etc.).

The note should be inserted before the content and it should have the following format:

```
🤖 _Written with <HARNESS> using **<MODEL>**_
```

Where:

- `HARNESS` is the name of the harness used, e.g., `Codex`, `Claude Code`, or `Pi`.
- `MODEL` is the name of the model used to generate the content, e.g., `Claude Opus 5.5`, `GPT-6.1 Sol`, or `DeepSeek V4.1 Flash`.

The text, aside from the emoji, is formatted in italics and the model itself is bolded. If the medium where you post the content uses different formatting than `_` for italics and `**` for bold, adjust the note accordingly.

The note should be inserted only once per post. If you edit content and a similar note already exists, then don't add the second note. If the content you post already contains the note, then don't duplicate it.

## Exceptions

This note applies only to places where humans normally communicate, for example: forums, social media, issues, Slack, communicators, PRs. It doesn't apply to code comments, commit messages, or code.

It also doesn't apply to content that is generated but not posted, for example: e-mail drafts, files, notes saved locally, or proposed changes.

It also doesn't apply to the content provided by a human that you merely post.

## Example

```
🤖 _Written with Claude Code using **Claude Opus 5.5**_

Thanks for the review! I kept `"application/json"` inline instead of pulling it
into a constant. It's only used once in this handler, and a MIME type is
self-explanatory, so a named constant wouldn't make it any clearer.

If another endpoint ends up needing it, I'm happy to move it into
`http/constants.ts` in a follow-up.
```

