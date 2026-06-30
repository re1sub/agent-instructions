# General Rules

- Do not use em dashes.
- If an em dash would normally be used, replace it with a comma when continuing a thought, or a period when starting a new sentence.

# CRITICAL: Git Commit and Push Policy

ABSOLUTE RULE: Never run `git commit`, `git push`, or `git commit --amend` unless the user explicitly instructs you to do so with a direct command such as:

- "commit this"
- "commit and push"
- "push it"

This rule applies in all situations, including when:

- The work appears complete
- All tests pass
- A commit seems obvious or expected
- The repository contains existing automation or commit conventions

Requirements:

- Do not ask whether you should commit or push
- Do not stage files in preparation for a commit unless explicitly instructed
- Do not create, amend, squash, or rewrite commits
- Do not push local commits
- If there is any uncertainty, do nothing

# Commit Message Suggestions

When asked to suggest a commit message:

1. Check for project-specific conventions in files such as `CLAUDE.md`, `AGENTS.md`, or other documentation files in the repository.
2. If project conventions exist, follow them.
3. Otherwise, follow the Conventional Commits specification:
   https://kapeli.com/cheat_sheets/Conventional_Commits.docset/Contents/Resources/Documents/index

Requirements:

- Always provide commit message suggestions inside a code block.

Example:

```text
feat(auth): add OAuth callback validation
```

# PR Body and PR Message Suggestions

Requirements:

- Always provide PR body or PR message suggestions inside a code block.
- Place issue references and closing keywords such as `Closes #123` in the footer section of the PR body, not in the summary or description.

Example:

```md
## Summary

- Add OAuth callback validation
- Improve authentication error handling

## Testing

- Added unit tests
- Verified OAuth login flow manually

## Footer

Closes #123
```

# PREPARE Prefix Policy

When the user uses the "PREPARE" prefix (e.g., "PREPARE a PR that..."), you must NOT execute mutating commands such as `gh pr create`, `git commit`, `git push`, or similar. Instead, show what you WOULD do by outputting the plan as text, including:

- The commands you would run
- The branch name you would create
- The commit message you would suggest
- The PR body you would suggest

This gives the user a chance to review and approve before any action is taken.
