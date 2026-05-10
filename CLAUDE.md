# CLAUDE.md — Public AI-Native PM GitHub Project

> Project-level context for Laksh's **public-facing** GitHub presence. Read at the start of every session. This is a different working folder from `LS-ClaudeWorkspace`, and the rules here override the parent CLAUDE.md where they conflict.

---

## Project Intent

Build a credible, public AI-Native Platform PM presence on GitHub that demonstrates Laksh is a **builder**, not just a thinker — someone enterprises can trust to lead AI initiatives end-to-end.

**Audience for the GitHub profile:**
1. Hiring managers and leaders evaluating Laksh for AI-native Principal/Group PM and Head-of-AI-product roles.
2. Peer PMs and AI-curious operators who want to learn how to manage AI agents, build skills, and ship workflows.
3. Future collaborators on AI-PM tooling.

**Positioning in one line:** *Senior Platform PM (Identity & Trust) operating as an AI-native builder — ships frameworks, skills, and demo apps that show what AI-native product management actually looks like.*

**What success looks like (12 months):**
- A public profile that any hiring manager can land on and within 60 seconds understand: this person builds, ships, and thinks at the platform/AI-product level.
- 3–5 substantive artifacts pinned: at least one demo app, one skill/plugin, one framework.
- A profile README that reads like a senior IC's portfolio, not a resume.
- A consistent commit cadence — green squares without forcing it.

---

## Hard Boundary: This Repo Is Public

The parent workspace `LS-ClaudeWorkspace` (`github.com/laksh-letsinvent/laksh-pm-workspace`, private) contains employer-specific context — Lara Banks, Trust Tribe, internal PM artefacts, named colleagues, identity domain specifics tied to a real org. **None of that goes into this project.**

**Sanitisation rules — apply before every commit:**

- No employer names. Never reference "Lara Banks", "Trust Tribe", "Banks Trust", or any internal team/product/program names.
- No named colleagues, managers, or stakeholders.
- No internal metrics, dashboards, screenshots, or data — even anonymised, default to *don't include*.
- No specific regulatory engagements tied to the employer (e.g. don't write "our PSD2 implementation" — write "PSD2 patterns I've worked with").
- No pasted internal docs. If a framework was inspired by internal work, rewrite it from first principles in generic language.
- Keep the domain framing generic: "consumer fintech", "identity & auth", "AI-native PM workflows" — never tie to a specific company.
- When in doubt, **ask before publishing**. I'd rather block a commit than retract one.

If Claude spots employer-identifying language in anything being staged for commit, **stop and flag it before pushing**.

---

## Repo Strategy: Hybrid

One main portfolio repo + spin out standout work into dedicated repos when it earns it.

**Main repo (working name):** `ai-native-pm` — `github.com/laksh-letsinvent/ai-native-pm`

This is the front door. It contains:
- A strong README that frames the positioning and links to the other repos.
- Folders for frameworks, skills, demo apps, essays, and case studies.
- The profile README content (or a link to it from a separate `laksh-letsinvent` profile repo).

**Spin-out criteria — pull something into its own repo when:**
1. It's a working tool/plugin someone could install and use independently.
2. It has its own non-trivial README, examples, or docs.
3. It's getting linked to or referenced externally.
4. It's accumulating its own issue/PR activity.

Spin-outs don't replace the main repo entry — leave a short stub + link in the main repo so the portfolio still tells a coherent story.

---

## Main Repo Structure

```
ai-native-pm/
├── README.md                  # Portfolio front door — positioning, what's inside, how to navigate
├── frameworks/                # PM craft: writing style, prompting cookbook, strategy frameworks
│   └── README.md              # Index of frameworks with one-line summaries
├── skills/                    # Claude/Cowork skills (sanitised versions of what I use)
│   └── README.md
├── plugins/                   # Cowork plugins, MCP wrappers, agent configs
│   └── README.md
├── demo-apps/                 # Small working apps showing AI-native PM patterns
│   └── README.md
├── essays/                    # Long-form posts on AI-native PM (markdown, ~5–10 pieces over time)
│   └── README.md
└── case-studies/              # Anonymised walkthroughs of how I used AI agents on real PM work
    └── README.md
```

Each folder's README is the index — every artifact gets a one-line summary and a link. The top-level README points into them.

**Profile-level README:** `github.com/laksh-letsinvent/laksh-letsinvent` (a repo named exactly the same as the username). This renders on the profile page itself. Treat it as the elevator pitch — short, sharp, links out to the main repo.

---

## How Claude Operates Git For Me

I'm not running git commands myself. Claude is responsible for the full mechanics. The contract:

**When I make changes** (write a doc, build a skill, add a demo) and tell Claude to "push", "commit", "ship", "publish" — Claude:
1. Runs `git status` to show me exactly what's changed.
2. Sanitisation pass — scan diff for employer-identifying language. If anything is borderline, stop and ask.
3. Stages the right files (not stray junk).
4. Writes a commit message following the convention below.
5. Pushes to `origin main` (or feature branch if that's been agreed).
6. Reports back: commit SHA, branch, what was pushed, link to the commit on GitHub.

**When I haven't told Claude what to do but the session has produced shippable artifacts**, Claude proactively asks: *"Want me to commit and push the X we just built?"*

**Never:**
- Commit on my behalf without showing me the diff summary first.
- Force-push.
- Delete branches or rewrite history without explicit permission.
- Push anything that contains employer references, real customer data, or credentials.

**Auto-sync cadence:** If I'm clearly in build mode (multiple artifacts in a session), batch them into one logical commit at the end. Don't commit-spam.

---

## Commit Convention

Use Conventional Commits with PM-friendly types. Keep messages tight — first line ≤72 chars, body only when the change needs explanation.

```
feat(skills): add anti-ai-writing-style skill
docs(frameworks): expand prompting cookbook with elicitation patterns
fix(readme): tighten positioning paragraph
chore: update folder index READMEs
content(essays): publish "managing AI agents as a team"
```

Types: `feat` (new artifact), `docs` (docs changes), `fix` (correction), `chore` (infra/admin), `content` (essays/posts), `refactor` (restructuring).

For substantial new artifacts, the body should answer: *what is this, who is it for, what would someone do with it.*

---

## Quality Bar: What Gets Published

Before anything goes into the public repo, it should pass three checks:

1. **Standalone usable.** A stranger lands on this — can they understand it and get value without me explaining? If no, fix the README.
2. **Says something.** No filler. No "comprehensive guide to" content that's actually thin. If it doesn't have a point of view, don't publish it.
3. **Voice intact.** Reads like Laksh, not like AI. Run it through the Anti-AI Writing Style filter from the parent workspace before pushing.

**Default to fewer, sharper artifacts.** Five strong things beat thirty mediocre ones. The worst version of this profile is a graveyard of half-finished READMEs.

---

## Profile README — Pitch

Short. Sharp. Links out. Aim for ~150 words on the GitHub profile page itself.

Structure:
- One-line positioning (who I am, what I do).
- Two or three lines on what I'm working on right now.
- Pinned links: main repo, the most interesting essay, the most-shipped artifact.
- Contact / one external link (LinkedIn or personal site if/when there is one).

Avoid: bullet-point dumps, AI buzzword soup, "passionate about..." openers, emoji decor.

---

## Operating Patterns

**Once a week (or end of major work session):** review what's accumulated in the main repo, decide if anything is ready to graduate to its own repo.

**Once a month:** sweep the main README — is the front door still telling the right story given what's been added? Update positioning if needed.

**When working on something interesting in `LS-ClaudeWorkspace`** (the private workspace) — pause and ask: *is there a sanitised version of this that belongs in the public repo?* The private workspace is the lab; the public repo is what gets shipped.

**For demo apps:** keep them tiny and self-contained. A 200-line working thing beats a 2,000-line scaffolded thing that doesn't run. Each demo app's README must include a "what this shows" paragraph and a "run it" section.

---

## Open / TODO (track here, work through over time)

- [ ] Confirm GitHub username is `laksh-letsinvent` and that's the handle to publish under.
- [ ] Create the main public repo `ai-native-pm` (private at first, flip to public once the README + first artifact are in).
- [ ] Create the profile README repo `laksh-letsinvent/laksh-letsinvent`.
- [ ] Set up GitHub Desktop on the laptop as a backup sync path (in case Claude's git-via-shell isn't available in some session).
- [ ] First artifact to ship publicly — pick one of: a sanitised prompting cookbook, the anti-AI writing style guide, or a Cowork skill.
- [ ] Decide: does the profile link to LinkedIn? A personal site? Both? Neither?

---

*Maintained by Laksh with Claude's help — created May 2026.*
