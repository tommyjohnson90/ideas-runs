# ideas-runs

Tom's ideas workspace, shared by the P620 and the X1. Clone it as `~/Dev/ideas`; the `ideas` plugin runs its agent teams here.

| Path | What it is |
| :- | :- |
| `.claude/settings.json` | turns on agent teams for this folder only; read access to everything except secret files; writes only to `runs/` |
| `runs/<slug>/<date>-<mode>/` | one folder per interview, research, critique or board run (brief, findings, report, `sources.md`) |
| `runs/.../sources/<repo>/` | that run's fresh copy of a project repo, renamed so its CLAUDE.md, AGENTS.md and `.claude/` don't load; ignored by git |

## Once per machine

```bash
cd ~/Dev
[ -d ideas ] && mv ideas ideas.old        # only if an older ~/Dev/ideas exists
gh repo clone tommyjohnson90/ideas-runs ideas
cd ideas && claude                        # accept the trust prompt once, then /exit
```

Accepting the trust prompt matters: until then Claude Code ignores this folder's allow rules (the deny rules for secrets always apply). If `ideas.old/runs` held runs, copy them in with `cp -rn ideas.old/runs/. runs/`, then commit and push.

## Every run

The skills do this for you, so this is only what happens:

- **Start:** `git pull --ff-only`, so a run begun on the other machine carries on here.
- **End:** the run folder is committed and pushed. Only the run folder is saved; its `sources/` copies and anything secret stay local.

If a pull or push fails (offline, or both machines saved at once), run `git status`, then `git pull --rebase && git push`.
