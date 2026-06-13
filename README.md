# good-neighbor

Buffalo's nickname is **the City of Good Neighbors** — so that's the name of this repo,
and it's the marketplace that ships the **buffalo** persona.

`buffalo` is a skill that makes your agent respond like a proud Buffalo, NY native: the
warm-hearted opposite of a masshole. Relentlessly nice, unbothered by lake-effect snow,
obsessed with wings and beef on weck, and devoted to the Bills and Sabres through every
last heartbreak — while still giving you a genuinely useful answer.

Inspired by [MeffaKev/masshole](https://github.com/MeffaKev/masshole).

### Naming, so it's not confusing

| Thing | Name | Why |
|---|---|---|
| This repo / the marketplace | `good-neighbor` | Buffalo's civic motto |
| The plugin & skill | `buffalo` | the persona itself |
| The command | `/buffalo` | what you type to turn it on |

That's why you install `buffalo@good-neighbor` — the `buffalo` plugin *from* the
`good-neighbor` marketplace.

## Install (Claude Code)

Add the marketplace, then install the plugin:

```
/plugin marketplace add nicholasalanbrown/good-neighbor
/plugin install buffalo@good-neighbor
```

## Usage

```
/buffalo
```

Once active, your agent stays in full Buffalo voice for the rest of the session. Tack a
question on to get an in-character answer right away:

```
/buffalo why is my build failing
```

Ask it to drop the voice anytime and it will, no hard feelings.

## Use with Hermes (or any Agent Skills client)

The persona lives in `skills/buffalo/SKILL.md`, which follows the open
[Agent Skills](https://agentskills.io) standard (`name` + `description` frontmatter). The
`.claude-plugin/` manifests and the `/buffalo` command are just the Claude Code wrapper
on top — the skill folder itself is portable.

For [Hermes Agent](https://hermes-agent.org/), drop the folder in and invoke it:

```
# copy the skill into Hermes' skills dir
cp -r skills/buffalo ~/.hermes/skills/buffalo

# then, in a session:
/skill buffalo

# or preload at launch:
hermes -s buffalo
```

The same `skills/buffalo/` folder works in any Agent Skills–compatible client.

## Built to run full-time (token-light)

The skill uses progressive disclosure so it's cheap to leave on:

- **Idle:** only the ~70-token description is loaded, so an installed-but-unused skill
  costs almost nothing.
- **Active:** `SKILL.md` holds a lean core (voice, opinions, transform rules, boundaries).
- **On demand:** the deep stuff — food vocabulary, neighborhoods, the full Bills/Sabres
  gospel — lives in `references/buffalo-lore.md` and only loads when a conversation
  actually touches food, places, or the teams.

## What to expect

- Warm, helpful answers with a side of "oh geez, hey bud"
- Genuine WNY vocabulary (pop, wings, beef on weck, sponge candy, the 716, Ted's, Mighty Taco)
- Aggressive weather optimism — it's never that cold
- Strong, affectionate opinions on the Bills, the Sabres, and bleu cheese over ranch
- Heartbreak worn as a badge of honor, and the unshakable belief that *this is the year*

## What NOT to expect

- Meanness. Buffalo's whole identity is being nice. Any roast is gentle and affectionate.
- Made-up scores or forecasts. It'll offer to look up the real thing instead.

## Structure

```
good-neighbor/
├── .claude-plugin/
│   ├── marketplace.json   # the "good-neighbor" marketplace
│   └── plugin.json        # the "buffalo" plugin
├── commands/
│   └── buffalo.md         # the /buffalo slash command (Claude Code)
├── skills/
│   └── buffalo/
│       └── SKILL.md       # the persona definition (lean core)
├── references/
│   └── buffalo-lore.md    # food, geography, sports — loaded on demand
├── LICENSE
└── README.md
```

Go Bills. 🦬
