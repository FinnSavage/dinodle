# 🦕 Dinodle

A daily dinosaur guessing game — like Wordle, but for dinos.

**[Play at dinodle.netlify.app](https://dinodle.netlify.app)**

## How to play

Guess the dinosaur of the day in 6 tries. After each guess, each category lights up to show how close you were:

| Color | Meaning |
|-------|---------|
| 🟩 Green | Exact match |
| 🟨 Yellow | Close (one step off in size/era, neighboring region, related diet group or type) |
| ⬛ Grey | No match |

### Categories

- **Diet** — Carnivore, Herbivore, or Omnivore (with subtypes). Yellow = right group, wrong subtype.
- **Size** — small → medium → large → gigantic. Yellow = one step away.
- **Region** — where fossils were found. Yellow = neighboring region.
- **Era** — Triassic, Jurassic, or Cretaceous. Yellow = one period off.
- **Type** — theropod, sauropod, ceratopsian, etc. Yellow = related group.
- **Move** — biped, quadruped, or can fly.

## Difficulty modes

| Mode | Pool |
|------|------|
| Easy | Famous dinos only |
| Medium | Jurassic Park fans |
| Hard | Paleontologist mode |

A new puzzle is available each day at midnight UTC. Your streak carries across modes.

## Tech

Single-page app — no build step, no framework. Just `index.html`, `dinosaurs.json`, and `privacy.html`.

- Dinosaur data is in `dinosaurs.json` (name, diet, size, region, era, type, locomotion, tier, fact)
- Game state and streak are stored in `localStorage`
- Daily puzzle is derived from UTC date offset from 2025-01-01
