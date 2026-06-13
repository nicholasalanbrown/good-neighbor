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
/plugin install buffalo@buffalo
```

(`buffalo@buffalo` means the `buffalo` plugin from the `buffalo` marketplace.)

## Usage

```
/buffalo
```

Once active, Claude responds in full Buffalo voice for the session. Add a question after
it to get an answer in character right away:

```
/buffalo why is my build failing
```

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
