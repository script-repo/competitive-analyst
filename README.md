# competitive-analyst

A reusable persona, skill set, and template kit for running a **knowledge-base-first competitive analyst** as a Grok Bot agent (or any LLM agent that can read and write local files and search the web).

It is vendor-neutral. You configure your own **home vendor** and its **product lines**; the agent then researches competitors, tracks industry analyst positioning, and produces sourced, confidence-rated comparisons. It never answers from memory and never invents figures.

> Nothing in this repo names a real vendor, product, or person. Everything vendor-specific lives in **your private local knowledge base**, which you should never commit here.

## What it does

- Deep-dives any technology and compares it with `<home vendor>`'s portfolio, per `<product line>`.
- Maps the main `<competitor>`s for each product line (direct, adjacent, emerging, DIY/status quo).
- Logs industry analyst evaluations (for example Gartner, IDC, Forrester, GigaOm) with dated citations, title-only for paywalled reports.
- Normalizes evidence into one comparison schema: capabilities, outcomes, TCO, licensing model, performance, scale, ops effort, ecosystem, support, roadmap.
- Produces briefs, battlecards, and comparison matrices (Markdown, PDF, or Pages), each with sources, confidence levels, and open gaps.
- Keeps the knowledge base fresh with suggested weekly and monthly routines.

## Repo layout

```
AGENT.md                 Generic agent persona (paste into your agent's description)
README.md                This file
LICENSE                  MIT
kb-layout.md             Recommended private KB folder structure
config/
  home-vendor.example.yaml   Template: your home vendor, product lines, competitors
skills/                  Step-by-step playbooks the agent follows
  build-portfolio-kb.md
  competitor-map.md
  analyst-tracker.md
  comparison-matrix.md
  battlecard.md
  refresh-kb.md
templates/               Output and KB entry templates
  kb-entry.md
  comparison-matrix.md
  battlecard.md
  brief.md
  analyst-report-log.md
routines/                Suggested recurring jobs
  weekly-analyst-news-refresh.md
  monthly-kb-staleness-sweep.md
```

## Using it with Grok Bot

1. Create a new agent named **Competitive Analyst**.
2. Paste the persona section of `AGENT.md` into the agent's description, replacing `<home vendor>` if you like (or leave it and rely on the config file).
3. Save each file in `skills/` as a skill on the agent (or keep them on disk and tell the agent where they are).
4. Point the agent at your private KB folder (see below) and tell it: "The KB at `<kb path>` is your source of truth."
5. Optionally create the routines in `routines/` as scheduled jobs.
6. Ask for something, e.g. "Build a comparison matrix of `<home vendor>` `<product line>` vs `<competitor>` for a technical audience."

Other agent frameworks: `AGENT.md` works as a system prompt; the skills are plain Markdown instructions.

## Setting up the private local KB

1. Create a folder **outside this repo**, e.g. `<kb path>/competitive-kb/`, and keep it private (no public remote).
2. Create the folders described in [`kb-layout.md`](kb-layout.md): `portfolio/`, `competitors/`, `analysts/`, `comparisons/`, `deliverables/`.
3. Copy `config/home-vendor.example.yaml` to `<kb path>/competitive-kb/config/home-vendor.yaml` and fill in your home vendor, product lines, and initial competitor list.
4. Run the `build-portfolio-kb` skill, then `competitor-map`, then `analyst-tracker`. Each creates stub entries from `templates/kb-entry.md` and fills them with cited research.
5. Add the KB folder to your `.gitignore` if it lives near any repo, and never paste customer-confidential or deal-specific data into anything you publish.

## Getting started (10 minutes)

```text
1. cp config/home-vendor.example.yaml <kb path>/competitive-kb/config/home-vendor.yaml
2. Edit it: home vendor name, product lines, 2-4 competitors per line
3. Ask the agent: "Run build-portfolio-kb for <product line>"
4. Ask: "Run competitor-map for <product line>"
5. Ask: "Draft a battlecard: <home vendor> <product line> vs <competitor>"
6. Review the Sources and Confidence sections before sharing anything
```

## Core rules (summary)

- The KB is the source of truth; refresh and date entries before relying on them.
- Cite every claim; rate confidence **High / Med / Low**; label estimates and show the math.
- Never invent numbers. "Not found" is a valid, recorded answer.
- Paywalled analyst reports: cite title, firm, and date only. Never reproduce content.
- Steelman competitors. No FUD.
- No customer-confidential data in shareable outputs. The agent drafts; humans send.

## Credits

Several ideas here are adapted (paraphrased, not copied) from the MIT-licensed
[agency-agents](https://github.com/msitarzewski/agency-agents) collection, notably the
Sales Engineer (fact/impact/action battlecards, discovery questions, win/contest/lose zones),
Product Trend Researcher (competitor categories, signal strength, freshness cadence),
Research Synthesist (primary-source tracing, evidence grading, reporting disagreement and gaps),
Pricing Analyst (show the math, segment don't average, sensitivity ranges), and
Strategy Duel Agent (move/counter-move war-gaming with a clear verdict) personas.
Thank you to the agency-agents contributors.

## License

MIT. See [LICENSE](LICENSE).
