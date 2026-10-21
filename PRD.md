# PRD — 2010

> Product requirements for `year-of-ai/2010`, a self-growing knowledge base about the year 2010.
> Sources: [README.md](README.md), [CLAUDE.md](CLAUDE.md), `_config.yml`, and the hub
> [`year-of-ai/year-of-ai.github.io`](https://github.com/year-of-ai/year-of-ai.github.io). Unknowns are marked **TBD**.

## 1. Overview / problem

`2010` is a **self-growing knowledge base** about the year 2010, one member repo of the
[`year-of-ai`](https://github.com/year-of-ai) lineage. It provides a readable, encyclopedic
reference that grows over time without a human writing each article.

This repo holds only its own content, a GitHub Pages `_config.yml` (a `remote_theme`
consumer of `bamr87/zer0-mistakes`), the `.claude/` adapter toolkit and `telemetry/`.
Growth is orchestrated **centrally by the hub** (`year-of-ai/year-of-ai.github.io`): on each tick the hub stages
the agent framework and this repo's concept seed, runs a Haiku → Sonnet → Opus
escalation to research and write content, and publishes only new content and
telemetry back here (see CLAUDE.md).

## 2. Target users

- Readers who want a neutral, sourced overview of the year 2010 (published at https://year-of-ai.github.io/2010).
- Maintainers of the `year-of-ai` lineage who operate the hub's growth loop.
- Specific audience segments / personas: **TBD**.

## 3. Goals and non-goals

**Goals**
- Cover the year 2010 across the seed's taxonomy categories with factual, neutral,
  encyclopedic, third-person articles.
- Verify every fact against at least two sources (CLAUDE.md convention).
- Publish as a static GitHub Pages site with no theme code in this repo.

**Non-goals**
- Holding the seed, growth policy, or agent framework (these live in the hub).
- Theme files (`_layouts`, `_includes`, `_sass`) — the theme is remote.
- Opinion, commentary, or unsourced content.

## 4. Core features (current)

- Static site: Jekyll with `remote_theme: bamr87/zer0-mistakes`, `baseurl: /2010`.
- Content by taxonomy category (Markdown files with `title` / `date` / `category` front matter):

| Category directory | Markdown files |
|---|---|
| `_posts/arts-culture/` | 16 |
| `_posts/history-politics/` | 23 |
| `_posts/people/` | 19 |
| `_posts/science-technology/` | 27 |
| `_posts/society-economics/` | 18 |

- Index/navigation documents at root: `README.md`, `TIMELINE.md`, `news.md`, `CLAUDE.md`, `LICENSE`.
- `telemetry/` growth ledger written by the hub's growth ticks.
- `.claude/` thin adapters (skills/commands) pointing at hub-staged procedures.

## 5. Requirements

**Functional**
- FR1: Each topic is a single Markdown file in its category directory with required front matter (`title`, `date`, `category`).
- FR2: The site builds on GitHub Pages using the remote theme and `_config.yml` alone.
- FR3: Growth ticks add content and telemetry only; they do not change the seed or framework here.
- FR4: Root index pages (README/TIMELINE) link to published articles.

**Non-functional**
- NFR1: Accuracy — every fact verified against ≥2 sources; neutral tone.
- NFR2: Minimal footprint — no theme code, no build tooling beyond Pages.
- NFR3: Traceability — every growth tick leaves a telemetry record.
- Performance, accessibility, and availability targets: **TBD**.

## 6. Success metrics (proposed — not defined in sources)

- Article count and coverage per category (baseline in the table above).
- Share of articles with ≥2 cited sources.
- Pages build success rate.
- Reader traffic: **TBD** (no analytics source found in the repo).

## 7. Roadmap / open questions

- README status line: Mature — this repository covers the year 2010. Succeeded by [year-of-ai/2011](https://github.com/year-of-ai/2011).
- README states this repo was **consolidated into `year-of-ai/2005-2011`** and is archived/read-only, but the GitHub repo is not archived and `year-of-ai/2005-2011` does not currently resolve on GitHub. Which is authoritative? **TBD**
- Lineage: spawned from `year-of-ai/2009` (per README).
- Target size / completion criteria for this year: **TBD** (governed by the hub's growth policy).
- Roadmap is owned by the hub; see `year-of-ai/year-of-ai.github.io`.

## 8. Links

- [README.md](README.md) · [CLAUDE.md](CLAUDE.md) · [TIMELINE.md](TIMELINE.md)
- Live site: https://year-of-ai.github.io/2010/
- Hub: https://github.com/year-of-ai/year-of-ai.github.io
- CHANGELOG: none in this repo (last commit 2026-10-03).
