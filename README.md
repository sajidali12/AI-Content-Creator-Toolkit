# AI Content Creator Toolkit

A Claude Skill that helps creators decide **what to publish next**: it finds and verifies topics, scores ideas with a transparent rubric, and turns the winner into a script, outline, or content calendar.

It works for any niche (travel, food, education, tech, gaming, fitness, business, podcasts, faceless channels, local businesses) and any format (Reels, Shorts, TikTok, long-form video, blogs, podcasts).

## Quick install

**Claude Code** (one command):

```bash
git clone https://github.com/sajidali12/AI-Content-Creator-Toolkit ~/.claude/skills/ai-content-creator-toolkit
```

Then ask: `What should I post next? My niche is budget travel in Pakistan.`

**Claude (web and desktop apps):**

1. Download `ai-content-creator-toolkit.zip` from the [latest release](https://github.com/sajidali12/AI-Content-Creator-Toolkit/releases/latest).
2. In Claude, open **Settings → Capabilities** and make sure code execution and file creation are enabled.
3. Go to the Skills section, upload the ZIP, and enable the skill.
4. Ask: `Help me choose my next content topic. My niche is ...`

The UI labels change from time to time; see [Anthropic's Agent Skills documentation](https://docs.anthropic.com/en/docs/agents-and-tools/agent-skills/overview) for current steps and plan availability.

## Example

**Prompt**

> Score these ideas for my beginner photography channel: gear unboxing, phone night photography tutorial, my first paid shoot, camera settings explained.

**Output** (produced by Claude with this skill, abridged)

> **Context and assumptions:** Beginner photography channel, audience is people learning on a phone or entry-level camera, goal is growing a returning audience. No analytics were provided, so demand is inferred, not measured.
>
> | Rank | Idea | Score | Main trade-off |
> |---|---|---:|---|
> | 1 | Phone night photography tutorial | 87 | Crowded topic, so it needs a specific angle |
> | 2 | My first paid shoot | 84 | Strongest story, but depends on having usable footage |
> | 3 | Camera settings explained | 80 | High demand, low differentiation |
> | 4 | Gear unboxing | 47 | Weak fit for beginners and for a new channel |
>
> **1. Phone night photography tutorial (87)**
> - **Audience payoff:** A usable night photo tonight, with the phone they already own.
> - **Angle:** "Three night shots, one phone, no tripod": show the failed attempt first, then the fix.
> - **Format:** 60–90 second short, with a longer walkthrough if it lands.
> - **Effort:** Low. One evening, no extra gear.
> - **Why it scores well:** Top marks for audience relevance, clarity of promise, demonstration potential and feasibility. It loses points on differentiation.
>
> **2. My first paid shoot (84)**
> - **Audience payoff:** An honest look at what a first client job involves, including the mistakes.
> - **Angle:** What you charged, what went wrong, what you would do differently.
> - **Effort:** Medium to high. Needs client permission to show the work.
>
> **4. Gear unboxing (47)** falls below the 55 "deprioritize" line: beginners rarely search for unboxings from small channels, and it shows little of your own perspective.
>
> **Recommendation:** Make the phone night photography tutorial next. Keep "my first paid shoot" as the follow-up, since it is the idea only you can make.
>
> *Scores are editorial aids for comparing ideas. They do not predict views.*

## What makes it different from just asking Claude

- **A published scoring rubric.** Eight weighted dimensions (audience relevance, creator fit, differentiation, feasibility and more) scored out of 100, so you can see why an idea ranks where it does. See [`references/IDEA-SCORING.md`](references/IDEA-SCORING.md).
- **Hard gates.** An idea with an unverifiable claim, a stale trend premise, or copied material is not recommended, whatever its score.
- **Honest trend research.** Current-trend claims come with sources and dates. If live search is unavailable, the skill says so instead of inventing headlines.
- **No made-up numbers.** It does not invent search volume, view forecasts, or competitor metrics.
- **A consistent report format.** Every idea comes with audience payoff, angle, format, effort and score, and the report ends with one clear recommendation.

## What you can ask

| You say | It does |
|---|---|
| "What should I post next?" | Generates, filters, scores and ranks ideas for your niche |
| "What's trending this week in ...?" | Researches current signals with sources and dates |
| "Help me find my niche" | Builds content pillars and an audience strategy |
| "Turn this into a Reel / Short / video / blog" | Writes hooks, a script or outline, and visual beats |
| "Make a 30-day content plan" | Builds a calendar that respects your real capacity |
| "Analyze my content" | Reads your metrics and proposes experiments |

More sample prompts and expected behavior are in [`references/EXAMPLES.md`](references/EXAMPLES.md) and [`evals/TEST-CASES.md`](evals/TEST-CASES.md).

## Repository structure

```text
├── SKILL.md                  # the skill: workflows, report format, guardrails
├── references/
│   ├── IDEA-SCORING.md       # weighted rubric and hard gates
│   ├── RESEARCH-PLAYBOOK.md  # trend verification and source quality
│   ├── FORMATS-AND-STORYTELLING.md
│   ├── ANALYTICS-AND-EXPERIMENTS.md
│   └── EXAMPLES.md
├── templates/
│   └── CONTENT-CALENDAR.md
└── evals/
    └── TEST-CASES.md
```

## Limitations

- Live trend research needs web search in your Claude environment.
- The skill cannot see your private channel analytics; paste the numbers in or connect a tool.
- Platform features and policies change. Verify official guidance when exact details matter.
- Always review facts, rights, disclosures and safety before publishing.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Niche-specific playbooks, real example outputs and new evaluation cases are especially welcome.

If this skill saved you time, a star helps other creators find it.

## License

MIT. See [LICENSE](LICENSE).
