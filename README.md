# Hi, I'm Antoni

📍 **Copenhagen** | 🤖 **Vibe coding with Claude Code** | 🔬 **Learning in public**

![Swift](https://img.shields.io/badge/-Swift-FA7343?style=flat-square&logo=swift&logoColor=white)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Shell](https://img.shields.io/badge/-Shell-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white)
![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Electron](https://img.shields.io/badge/-Electron-47848F?style=flat-square&logo=electron&logoColor=white)
![Claude](https://img.shields.io/badge/-Claude_Code-000000?style=flat-square&logo=anthropic&logoColor=white)
![macOS](https://img.shields.io/badge/-macOS-000000?style=flat-square&logo=apple&logoColor=white)

> 11 projects, 6,400 sessions, 29,000 messages -- all with Claude Code since Jan 2026. Every repo below was an experiment in how far AI-assisted development can go, and where it breaks.

## Projects

Each one-liner is the lesson, not the feature.

- 🐭 **[pocket-gris](https://github.com/aharbuz/pocket-gris)** - Built a 180-test, 48-commit macOS app entirely through Claude Code to find the limits of AI-guided native Swift development
- 👁️ **[look-awry-xcode](https://github.com/aharbuz/look-awry-xcode)** - Same app, attempt 1: GUI-first with Xcode -- shipped fast, 0 tests, taught me that speed without feedback loops is a trap
- 👁️ **[look-awry-spm-cli](https://github.com/aharbuz/look-awry-spm-cli)** - Same app, attempt 2: CLI-first with SPM -- slower start, 98 tests, proved that Pure Core + GUI Adapter is the sweet spot for AI development
- 👁️ **[look-awry-electron](https://github.com/aharbuz/look-awry-electron)** - Same app, attempt 3: Electron + Playwright -- 252 tests, best AI feedback loops, worst resource usage. The definitive tradeoff comparison
- 🔧 **[claude-wrap](https://github.com/aharbuz/claude-wrap)** - 4 hooks that changed everything: context guard, session export, auto-wrap-up, plan verifier -- because Claude Code's biggest problem is session management
- 📄 **[pdf-tool](https://github.com/aharbuz/pdf-tool)** - 3 commits, no tests, empty PROGRESS.md -- the control group that proved documentation discipline matters
- 🖱️ **[field-mouse](https://github.com/aharbuz/field-mouse)** - My first vibe-coded project. Next.js vector field. Zero process, pure vibes. The "before" picture

## The Look-Awry Meta-Lesson

I built the same eye break timer 3 times to compare architectures for AI-assisted development:

| | Xcode (GUI-first) | SPM (CLI-first) | Electron |
|---|---|---|---|
| Tests | ~0 | 98 | 252 |
| AI feedback speed | Slow (manual) | Medium (CLI) | Fast (Playwright) |
| Maintainability | Hardest | Easiest | Good |
| Resource usage | 20-50 MB | 20-50 MB | 100-300 MB |

**Takeaway:** Native Swift has the best UX but the worst AI feedback loops. Electron has the best feedback loops but the worst footprint. CLI-first SPM is the sweet spot.

## What I Learned

Patterns that survived 11 projects and 6,400 sessions:

**Architecture**
- **Pure Core + GUI Adapter** -- zero UI deps in core. Single biggest win across all projects
- **CLI-first verification** -- sub-second feedback without launching a GUI
- **Phase-based development** -- each phase independently shippable, git history stays readable

**Working with Claude Code**
- **CLAUDE.md is expensive** -- it loads on every request. Keep it lean, push reference material to skills
- **Hooks beat instructions** -- context guard, auto-wrap-up, plan verifier have zero cost until triggered
- **Session timeouts are the #1 problem** -- 54 partially-achieved sessions. Mitigated with continuation prompts and incremental commits
- **Claude acts when you need it to plan** -- the most common friction point. Fixed with explicit CLAUDE.md rules and a plan-verifier hook
- **Sub-agent economics** -- use Sonnet for parallel sub-tasks, Opus for orchestration. Real cost savings

**Process**
- **Commit to a stack early** -- 3 failed Storybook installs, multiple sessions on dead-end NSPopover automation
- **Continuous quality, not late audits** -- 16 bugs accumulated in 2,000 lines before a single review pass caught them
- **Bash for hooks, TypeScript for pipelines** -- learned this the hard way with GNU/macOS shell incompatibilities

## Stats

```
Sessions:      6,393
Messages:     29,045
Tool calls:   84,000+ (mostly browser automation)
Jobs processed:  386+ (via unified-job-search-bot, not public)
```

## Workflow Evolution

```
Jan 2026:  Pure vibes. No docs, no structure.
     ↓
Feb early: AGENTS/ folder, PROGRESS.md, phase-based development.
     ↓
Feb mid:   Hooks, context guards, continuation prompts, sub-agent patterns.
     ↓
Feb late:  Every CLAUDE.md rule traces back to a specific failure.
```

---

*All projects built with [Claude Code](https://claude.ai/claude-code). The retrospective and insights data come from analyzing 29K messages across 6.4K sessions.*
