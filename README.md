# Spring Break 2027 News

The news subdomain of springbreak.com: **news.springbreak.com**. A single page that covers Spring Break 2027 peak weeks, top-ranked destinations, package prices, confirmed lineups and local beach rules. It uses springbreak.com's colors, fonts and "Ask with" AI picker. Everything lives in `index.html`: no build step and no dependencies.

## Features

- **Prefilled prompts:** 15 prompt chips in the Ask AI section (plus 4 quick-start chips in the hero) fill in the question box. Destination, week, group size and city are added to the prompt.
- **"Ask with" AI picker:** Claude, ChatGPT, Perplexity, Copilot, Grok or Google AI Mode. Every ✦ button opens the chosen assistant with a prompt that asks for sources, publish dates and the latest info. The choice is shared with springbreak.com's `sb27-engine` setting.
- **Copy prompt** on every card.
- Top stories, 2027 calendar, top 10 destinations, package prices, lineups, beach rules and FAQ.
- Light and dark mode, same tokens as springbreak.com.

## Updating the news

All content is at the top of the `<script>` in `index.html`:

| What | Variable |
|---|---|
| Headline cards | `stories` |
| Peak weeks | `weeks` |
| Top 10 ranking | `destinations` |
| Package prices | `prices` |
| Concert & DJ lineups | `lineups` |
| Beach rules | `rules` |
| Prompt chips | `promptGroups` |
| AI assistants | `ENGINES` |

Photos are in `assets/img/`. News compiled November 23, 2026.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Domain

`CNAME` points GitHub Pages at `news.springbreak.com`. At the DNS host, add a `CNAME` record for `news` pointing to `electronbender.github.io`.
