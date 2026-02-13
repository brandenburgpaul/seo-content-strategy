# seo-content-strategy

A Claude Code skill for SEO content strategy workflows — keyword analysis, on-page scoring, meta tag generation, internal linking suggestions, and content gap analysis.

## Features

| Task | Description |
|------|-------------|
| `keyword-analysis` | Analyze keyword CSV exports from Ahrefs, SEMrush, GSC, etc. Find opportunities, clusters, and quick wins. |
| `onpage-score` | Score existing content against 10 on-page SEO factors. Get a letter grade and prioritized fixes. |
| `meta-generation` | Generate optimized title tags, meta descriptions, and OG tags with character counts. |
| `internal-linking` | Get internal linking suggestions with anchor text, target pages, and relevance scores. |
| `content-gap` | Compare your content against competitors to find missing topics, keywords, and content types. |

## Installation

### Option 1: Project-level (recommended)

Add the skill to a specific project so it's available when working in that repo:

```bash
# From your project root
mkdir -p .claude/skills
cp -r seo-content-strategy .claude/skills/
```

### Option 2: User-level (global)

Install globally so the skill is available in all projects:

```bash
mkdir -p ~/.claude/skills
cp -r seo-content-strategy ~/.claude/skills/
```

### Option 3: Clone from GitHub

```bash
# Project-level
git clone https://github.com/brandenburgpaul/seo-content-strategy.git .claude/skills/seo-content-strategy

# User-level
git clone https://github.com/brandenburgpaul/seo-content-strategy.git ~/.claude/skills/seo-content-strategy
```

## Usage

Invoke the skill in Claude Code using the slash command:

```
/seo-content-strategy keyword-analysis keywords.csv
/seo-content-strategy onpage-score ./content/blog-post.html
/seo-content-strategy meta-generation ./content/landing-page.md
/seo-content-strategy internal-linking ./content/guide.md
/seo-content-strategy content-gap competitor-keywords.csv
```

You can also invoke it without arguments and Claude will ask what you need:

```
/seo-content-strategy
```

## Input Formats

### Keyword Analysis

Accepts CSV files with columns such as:
- `keyword`, `search_volume`, `difficulty`, `cpc`, `position`, `clicks`, `impressions`, `ctr`, `url`
- Column names are detected automatically; various delimiter formats (comma, semicolon, tab) are supported.

See [`examples/keyword-analysis-input.csv`](examples/keyword-analysis-input.csv) for a sample.

### On-Page Scoring

Accepts HTML files or Markdown content files.

### Meta Generation

Accepts any content file (HTML, Markdown, plain text).

### Internal Linking

Accepts a content file. Optionally provide additional file paths or a sitemap for site structure context.

### Content Gap Analysis

Accepts:
- A CSV of competitor keywords
- A list of your existing content URLs
- A topic brief or content plan document

## Examples

The `examples/` directory contains sample inputs and expected outputs:

| File | Description |
|------|-------------|
| `keyword-analysis-input.csv` | Sample keyword export CSV |
| `keyword-analysis-output.md` | Expected analysis output |
| `onpage-seo-scoring.md` | Sample on-page SEO score report |
| `meta-generation.md` | Sample meta tag generation output |
| `internal-linking.md` | Sample internal linking suggestions |
| `content-gap-analysis.md` | Sample content gap report |

## 🚧 Active development — keyword analysis and on-page scoring are battle-tested, other capabilities improving rapidly

## License

MIT
