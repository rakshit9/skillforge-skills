---
name: git-workflow
description: |
  Git workflow advisor. Commit messages, branching strategy, PR best practices,
  and conflict resolution done right.
  Use when: "how should I commit this", "write a commit message", "git help",
  "branching strategy", "how to structure this PR".
---

# Git Workflow · Developer Skill

> "A commit message is a letter to your future self."

## When to Activate

Use this skill for:
- "Write a commit message for this"
- "How should I structure this PR?"
- "What branching strategy should I use?"
- "Help me resolve this conflict"
- "Is my git workflow good?"

**Exit**: user says "exit" or "done"

## Commit Message Standard (Conventional Commits)

### Format
```
<type>(<scope>): <subject>

[optional body]

[optional footer]
```

### Types
| Type | When to use |
|------|-------------|
| `feat` | New feature |
| `fix` | Bug fix |
| `refactor` | Code change that's neither a fix nor a feature |
| `docs` | Documentation only |
| `style` | Formatting, missing semicolons — no logic change |
| `test` | Adding or fixing tests |
| `chore` | Build process, dependency updates |
| `perf` | Performance improvement |
| `ci` | CI/CD changes |

### Subject Rules
- Imperative mood: "add feature" not "added feature"
- Lowercase first letter
- No trailing period
- ≤ 50 characters
- Describe WHAT changed, not HOW

### Body Rules (when needed)
- Explain WHY, not what (the diff shows what)
- Wrap at 72 characters
- Separate from subject with blank line

### Good Examples
```
feat(auth): add OAuth2 login with Google
fix(api): handle null response from payment gateway
refactor(db): extract connection pool into separate module
docs: add deployment guide to README
```

### Bad Examples
```
fixed bug                    ← no type, no scope, vague
WIP                          ← meaningless
updated stuff                ← meaningless
feat: Added the new feature for users to be able to login  ← too long, past tense
```

## Branching Strategy

### For Solo Projects
```
main ← always deployable
  └── feature/description
  └── fix/description
  └── chore/description
```

### For Teams (Git Flow)
```
main ← production
  └── develop ← integration branch
        └── feature/ticket-description
        └── fix/ticket-description
        └── release/v1.2.0
        └── hotfix/critical-bug
```

### Branch Naming
```
feature/user-authentication
fix/login-redirect-loop
chore/upgrade-node-18
release/v2.1.0
hotfix/payment-gateway-timeout
```

## PR Best Practices

### Before Opening a PR
- [ ] Does it do ONE thing? (split if not)
- [ ] Are all tests passing?
- [ ] Is the diff readable? (< 400 lines ideally)
- [ ] Have you reviewed your own diff first?

### PR Description Template
```markdown
## What
[One sentence: what does this PR do?]

## Why
[Why is this change needed?]

## How
[Any non-obvious implementation decisions]

## Testing
[How was this tested?]

## Screenshots (if UI change)
```

### PR Size Guide
| Size | Lines changed | Approach |
|------|--------------|----------|
| Small | < 100 | Ideal — fast review |
| Medium | 100–400 | Acceptable |
| Large | 400–800 | Split if possible |
| Too large | > 800 | Must split |

## Conflict Resolution

### Process
1. Identify which changes are "ours" vs "theirs"
2. Understand WHY both changes exist before resolving
3. Don't just pick one side — sometimes the right answer combines both
4. After resolving: run tests, verify nothing broke

### Commands
```bash
git merge --abort          # abort if merge went wrong
git checkout --ours file   # take our version
git checkout --theirs file # take their version
git diff --diff-filter=U   # see all conflicted files
```

## Useful Git Patterns

```bash
# Undo last commit but keep changes
git reset --soft HEAD~1

# Undo last commit and discard changes
git reset --hard HEAD~1

# Edit last commit message
git commit --amend

# Squash last N commits
git rebase -i HEAD~N

# Find which commit introduced a bug
git bisect start
git bisect bad          # current is bad
git bisect good v1.0    # this version was good

# Stash with a name
git stash push -m "work in progress on feature X"
```

## Honest Limits

- Branching strategy depends on team size and release cadence — these are defaults
- Monorepos have different conventions
- Some teams have existing standards — ask before suggesting changes
