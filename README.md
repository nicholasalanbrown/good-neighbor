# buffalo

A Claude Code skill that makes Claude respond like a proud Buffalo, NY native — the
warm-hearted opposite of a masshole. Relentlessly nice, unbothered by lake-effect snow,
obsessed with wings and beef on weck, and devoted to the Bills and Sabres through every
last heartbreak.

Inspired by [MeffaKev/masshole](https://github.com/MeffaKev/masshole).

## Installation

Add the marketplace, then install the plugin:

```
/plugin marketplace add nicholasalanbrown/good-neighbor
/plugin install buffalo@good-neighbor
```

(`buffalo@good-neighbor` means the `buffalo` plugin from the `good-neighbor` marketplace.)

## Usage

```
/buffalo
```

Once active, Claude responds in full Buffalo voice for the session. Add a question after
it to get an answer in character right away:

```
/buffalo why is my build failing
```

## Use with Hermes (or any Agent Skills client)

The persona lives in `skills/buffalo/SKILL.md`, which follows the open
[Agent Skills](https://agentskills.io) standard (`name` + `description` frontmatter).
That means it's portable — the `.claude-plugin/` manifests and the `/buffalo` slash
command are just the Claude Code convenience layer on top.

For [Hermes Agent](https://hermes-agent.org/), drop the skill folder in and invoke it:

```
# copy skills/buffalo into Hermes' skills dir
cp -r skills/buffalo ~/.hermes/skills/buffalo

# then, in a session:
/skill buffalo

# or preload at launch:
hermes -s buffalo
```

The same `skills/buffalo/` folder works in any Agent Skills–compatible client.

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
│   ├── marketplace.json
│   └── plugin.json
├── commands/
│   └── buffalo.md        # the /buffalo slash command
├── skills/
│   └── buffalo/
│       └── SKILL.md      # the persona definition
├── LICENSE
└── README.md
```

Go Bills. 🦬
