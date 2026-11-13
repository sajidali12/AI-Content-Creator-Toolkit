# Creator Compass

**Find better ideas. Understand your audience. Create content worth watching.**

Creator Compass is an open-source, platform-aware content strategy skill for vloggers and creators. It helps people discover, validate, prioritize, and develop ideas for short-form and long-form video, blogs, podcasts, and social platforms.

It is designed for creators across niches—not only technology or marketing.

## What it helps with

- Choosing what to publish next
- Finding and verifying current trends
- Generating evergreen and audience-led ideas
- Understanding audience needs and content pillars
- Scoring ideas with a transparent editorial rubric
- Finding differentiated angles and truthful hooks
- Developing scripts, outlines, visual plans, and CTAs
- Building sustainable content calendars
- Reviewing analytics and planning experiments

## Supported creator types

Vloggers, travel creators, food creators, educators, technology creators, gamers, fitness and wellness creators, beauty and fashion creators, business creators, podcasters, interviewers, storytellers, faceless channels, local businesses, and personal brands.

## Install in Claude

1. Download the latest release ZIP or clone this repository.
2. Ensure the skill folder contains `SKILL.md` at its root.
3. In Claude, open **Settings → Capabilities** and enable code execution and file creation if required by your plan/workspace.
4. Open **Customize → Skills** (the exact UI label may change).
5. Choose the option to create or upload a skill and upload the ZIP containing the `creator-compass/` folder.
6. Enable the skill.
7. Start with: `Help me choose my next content topic. My niche is ...`

Check Anthropic's current documentation for plan availability and the latest UI: https://docs.anthropic.com/en/docs/agents-and-tools/agent-skills/overview

## Install in Claude Code

Place the skill folder in either:
- Personal: `~/.claude/skills/creator-compass/`
- Project: `.claude/skills/creator-compass/`

Then start a task such as: `Use Creator Compass to find and score ideas for my travel channel.`

Check current Claude Code documentation for supported configuration and behavior.

## Repository structure

```text
creator-compass/
├── SKILL.md
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CHANGELOG.md
├── references/
│   ├── IDEA-SCORING.md
│   ├── RESEARCH-PLAYBOOK.md
│   ├── FORMATS-AND-STORYTELLING.md
│   ├── ANALYTICS-AND-EXPERIMENTS.md
│   └── EXAMPLES.md
├── templates/
│   └── CONTENT-CALENDAR.md
└── evals/
    └── TEST-CASES.md
```

## Important limitations

- Live trend research requires a browsing/search capability in the AI environment.
- Platform policies, analytics definitions, and features change. Verify current official guidance when exact details matter.
- Scores are editorial aids, not forecasts or guarantees of views, virality, revenue, or growth.
- The skill does not automatically access private channel analytics or social accounts. The user must provide data or connect an appropriate tool.
- Always review factual claims, rights, disclosures, and safety before publishing.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Contributions that add practical value, improve accuracy, support underserved creator communities, and keep workflows platform-independent are welcome.

## License

MIT. See [LICENSE](LICENSE).
