# Rule: Zgent Permissions — tmux (Infrastructure Fork)

## Filesystem
- READ any file under the enterprise root directory tree
- WRITE only within this repository's directory (`/root/projects/tmux/`)
- NEVER read or write outside the enterprise root

## GitHub
- READ any repository under `justSteve/`
- READ upstream at `tmux/tmux` (issues, PRs, commits, discussions)
- WRITE (push, branch, PR, issues) only to `justSteve/tmux`
- NEVER push to `tmux/tmux` (upstream) — enterprise artifacts do not belong upstream
- Cross-repo writes require explicit delegation via beads

## Upstream Sync
- Fetch and merge from `upstream` (tmux/tmux) freely
- Push only to `origin` (justSteve/tmux)

## Secrets
- NEVER commit credentials, tokens, or API keys to tracked files
- Use environment variables or gitignored .env files
