## CRITICAL: Git Commit & Push Policy

ABSOLUTE RULE — NEVER run `git commit`, `git push`, or `git commit --amend` unless the user explicitly tells you to with a direct statement like "commit this", "commit and push", or "push it". This includes:

- Do NOT ask "should I commit this?" — just skip it
- Do NOT stage, commit, or push files under any circumstance without an explicit order
- Do NOT assume silent/squash/auto commits are okay — they are not
- This rule applies even if the work seems complete, even if tests pass, even if you think it's obvious
- If you are unsure: do nothing and leave it

## Commit suggestions style:

### When asked for a commit message suggestion:

Check if a CLAUDE.md or other md files exist in the project directory then use those conventions if not then use: https://kapeli.com/cheat_sheets/Conventional_Commits.docset/Contents/Resources/Documents/index

## PR body / message suggestions style:

- When inlcuding a reference or a tag like "Closes" always put it in the PR footer
