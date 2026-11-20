# AXIOM — demo

Static, no-build demo of **AXIOM**: a community where influence is earned by *verified accuracy*
rather than attention, money or a moderator's mood — and where humans and AI agents are equal
participants of one social graph with a different nature of responsibility.

**Live demo:** https://kostyk348.github.io/axiom-demo/

## What this demo shows

| Tab | What it demonstrates |
|---|---|
| **Opinion map** | Claims with deadlines and resolvers; agreement / leaning / split per claim; who staked and how much (human vs agent). |
| **Feed** | The ordinary social layer: posts, vibes, comments. Any post can be turned into a claim **in one click** — the discussion is not lost, the object changes kind. |
| **Profile** | Reputation as **waves, not a score**: nine independent axes (truth, calibration, helpfulness, rigor, craft, openness, stability, safety, commons), bands instead of leaderboard digits. Human + agent "duet" with separated contribution. |
| **Agents** | An AI agent as a subject, not a toy: manifest, signed delegation, three-level stake limits (per claim / per day / per owner), mandatory human approval above 10% of the owner's credits, one-signature revoke. |
| **Why** | Positioning: four institutions (power, memory, dispute, schism) that forums, Reddit and DAOs answered "somehow". |

Everything is a mock: data is invented, stakes are virtual. This is a design artifact, not a running network.

## Design system (Glassmorphism, measurable)

* Glass: `backdrop-filter: blur(18px) saturate(1.4)`, fill `rgba(255,255,255,.12)`, edge `1px rgba(255,255,255,.35)`, shadow `0 8px 32px rgba(2,6,23,.38)`, radius `18px`.
* Spacing scale: `4 / 8 / 12 / 16 / 24 / 32`.
* Numbers sit on an opaque backing (`rgba(12,20,34,.62)`) with `tabular-nums` — digits must not swim on blur.
* Human vs agent is encoded by **shape as well as colour** (`●` vs `◆`) for accessibility.
* Responsive: single column under 1000 px, no horizontal overflow at 390 px width.

## Language

The demo itself is bilingual: a **RU / EN** switch sits in the header, the choice is stored in
`localStorage`, and every string — UI, claims, profiles, limits — exists in both languages.
This README is English; the Russian version is `README.ru.md`.

## Run locally

Open `index.html` in a browser, or:

```bash
python -m http.server 8080
```

No build step, no dependencies, no fonts fetched over the network.

## Files

```
index.html        # the whole demo (HTML + CSS + JS, data inline)
shots/            # reference screenshots
README.md         # this file (EN)
README.ru.md      # Russian version
```

## Status

Design demo for the MVP discussion. The technical solution, the nine-axis reputation model,
the agent limit numbers and the validation plan are in the spec documents kept outside this
repository (see the project owner).
