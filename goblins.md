# Goblin Threat System

Goblins are AI-controlled enemies that spawn dynamically based on depth and time. They are not decorative — they are a direct threat to your survival and unredeemed inventory.

## Spawn Rates

| Zone | First Spawn | Interval | Max Active |
|---|---|---|---|
| Surface (0–99m) | 90s | 22s | 7 |
| Deep (100–299m) | — | 12s | 12 |
| Abyss (300m+) | — | 7s | 18 |

A 10-second audio/visual warning plays before the first goblin spawns each session.

## Stats

| Stat | Regular | Alpha |
|---|---|---|
| HP | 3 | 12 |
| Damage | 15 | 20 (near alpha) |
| $GEM reward | 1 | 3 |
| Score reward | 150 | 350 |

## Behavior Types

Goblin AI becomes progressively more dangerous as you descend.

### Always Active
- **Basic Chase** — aggros within 20 tiles, pursues until 35 tiles away
- **Retreat & Regroup** — backs off 3 tiles after being hit, re-engages after 1.5 seconds
- **Goblin Herding** — pushes the player toward lava or other hazards

### Unlocks at 100m
- **Flanking** — a second goblin circles behind the player while the first attacks
- **Vertical Awareness** — goblins drop through openings and climb walls to pursue
- **War Parties** — every 2nd spawn cycle produces a coordinated group of 3–5 goblins simultaneously
- **Alpha Goblin** — 15% spawn chance; 12 HP, darker green color, buffs nearby goblins; their death causes nearby goblins to scatter for 3 seconds
- **Coordinated Surround** — when 3+ goblins are aggro, they spread to encircle the player

### Unlocks at 300m
- **Ambush** — holds position until player enters 6-tile range, deals +5 bonus damage on first strike
- **Cave Dwellers** — goblins move 15% faster on CAVE tiles
- **Enhanced Speed** — all goblins move 15% faster overall

## Alpha Goblin

The Alpha is a boss-tier goblin with 12 HP and a darker green appearance. While alive, nearby regular goblins deal extra damage and move faster. Killing the Alpha causes a 3-second scatter — use it to breathe and reposition.

**Alpha rewards: 3 $GEM + 350 score points**

## Survival Tips

- Always redeem inventory before pushing to a new depth zone
- Use terrain (walls, caves) to break line of sight
- Kill the Alpha first — it nerfs the pack
- At 300m+, never stand still in open caverns
