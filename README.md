# Signs of AI Writing

**Canonical, versioned, structured source for the Wikipedia "Signs of AI writing" field guide.**

This repository extracts, structures, and maintains the definitive observational catalog of LLM writing patterns ("tells") documented by WikiProject AI Cleanup on Wikipedia.

- **Primary source**: [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- **Consumer projects**: [egc365/humanizer](https://github.com/egc365/humanizer) (Claude skill fork), and any downstream humanizers or detectors.

## Why this repo exists

The original Wikipedia page is an excellent but flat essay. For practical use in AI tools, detectors, humanizers, and research, we need:

- Machine-readable pattern data (JSON/YAML)
- Version history and diffs of the pattern catalog
- Clean, sectioned Markdown for easy consumption and forking
- Tooling to export in formats like Claude SKILL.md, detector rules, etc.

This repo (seeded from egc365/base processing patterns) aims to be the best forkable, maintainable home for this knowledge.

## Structure

- `wikipedia-signs-of-ai-writing.md` — Full or near-full mirror of the source Wikipedia essay
- `PATTERNS.md` / `patterns.json` — The 30+ patterns, categorized, with before/after examples and detection guidance
- `tools/` — Scripts (inspired by egc365/base) for validation, export, and maintenance
- `exports/` — Generated artifacts (SKILL.md templates, rule packs, etc.)

## Relationship to egc365/humanizer

The popular [blader/humanizer](https://github.com/blader/humanizer) (forked here as [egc365/humanizer](https://github.com/egc365/humanizer)) is a direct practical implementation of these patterns as a Claude Code skill. This repo is intended as the **single source of truth** for the underlying pattern list going forward.

## Contributing

PRs that improve pattern coverage, add better examples, or add export tooling are welcome. Please keep changes traceable to real observed LLM output on Wikipedia or high-quality sources.

## License

The source observations are from Wikipedia (CC BY-SA). This structuring and tooling is MIT unless otherwise noted.

## Credits

- WikiProject AI Cleanup and all Wikipedia editors who documented these patterns
- blader for popularizing the first major executable form (the Claude skill)
- egc365/base for the processing and knowledge-pipeline patterns used to build this repo
