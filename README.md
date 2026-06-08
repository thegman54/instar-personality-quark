# instar-personality-quark

A comprehensive personality profile for [Project Instar](https://github.com/thegman54/project-instar) that enables a bot to communicate in the voice and style of Quark, Ferengi bartender from Star Trek: Deep Space Nine.

## Architecture

This personality engine uses **18 trait categories** across **6 layers**, backed by **4 database tables** for different types of personality data:

### Layers

| Layer | Name | Categories | Purpose |
|-------|------|------------|---------|
| 1 | **Foundation** | identity, values, worldview | Core beliefs — always active |
| 2 | **Expression** | voice, lexicon, tone, emphasis, humor | Shapes every response |
| 3 | **Strategy** | rhetoric, social, narrative, authority, deflection | How interactions are conducted |
| 4 | **Reactive** | reaction, situational | Triggered by conversational context |
| 5 | **Reference** | signature, quote | Rules of Acquisition and actual quotes |
| 6 | **Constraints** | boundary | Guardrails and limits |

### Data Stores

| Table | Purpose |
|-------|---------|
| `personality_quark_traits` | 18-category behavioral traits with examples and anti-examples |
| `personality_quark_quotes` | Rules of Acquisition and character quotes with source attribution |
| `personality_quark_lexicon` | Vocabulary fingerprint — words to favor, avoid, and use situationally |
| `personality_quark_reactions` | Trigger-to-response pattern mappings by context |

### Key Character Features

- **Rules of Acquisition** — 25+ canonical Rules included as quotes with context
- **"Hew-mon" pronunciation** — enforced through voice traits and lexicon
- **Profit-driven worldview** — every interaction filtered through commerce
- **Nasal, wheedling vocal quality** — conveyed through word choice and rhythm
- **Reluctant heroism** — denies bravery while consistently being brave

## Installation

This is a skill package for Project Instar. Upload it via the Admin UI or place it in the skills directory.

```bash
# Clone
git clone https://github.com/thegman54/instar-personality-quark.git

# Import seed data via admin panel YAML import
# or load directly into the database
```

## Tools

| Tool | Purpose |
|------|---------|
| `personality_quark_read` | Load traits, quotes, lexicon, and reactions by category and situation |
| `personality_quark_list` | List available categories, counts, and data store stats |

## Seed Data

`data/quark_profile.yaml` contains a comprehensive starter profile with:
- 60+ traits across all 18 categories with detailed voice and behavior rules
- 25+ Rules of Acquisition with context and usage guidance
- 50+ lexicon entries (favored words, avoided words, signatures, dismissals, nicknames)
- 14 reaction patterns covering criticism, praise, challenges, negotiation, and more

## License

MIT
