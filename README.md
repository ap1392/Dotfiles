# dotfiles

Personal config, version-controlled and symlinked into place.

## claude/

Claude Code config. The real files live here; `~/.claude/` holds symlinks pointing back.

| Repo file | Symlinked to | What it is |
|-----------|--------------|------------|
| `claude/CLAUDE.md` | `~/.claude/CLAUDE.md` | Personal instructions, auto-loaded in every project |
| `claude/settings.json` | `~/.claude/settings.json` | Model, hooks, permissions |
| `claude/skills/` | `~/.claude/skills/` | Custom personal skills (`/pr-description`, `/cleanup`, …) |

Only these are tracked — the rest of `~/.claude/` is machine-local runtime state
(history, sessions, caches) and is intentionally left out.

### Set up on a new machine

```bash
git clone <this-repo> ~/dotfiles
ln -s ~/dotfiles/claude/CLAUDE.md     ~/.claude/CLAUDE.md
ln -s ~/dotfiles/claude/settings.json ~/.claude/settings.json
ln -s ~/dotfiles/claude/skills        ~/.claude/skills
```

(If a real file already exists at one of those paths, move it aside first.)
