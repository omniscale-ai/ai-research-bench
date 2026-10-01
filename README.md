# Autoresearch in the Wild — evidence map

An interactive 3D illustration of **“AI-Research Agents in the Wild. From GitHub and arXiv to Regularities and Gaps”**
(Aleksey Komissarov & Andrey Ustyuzhanin, [arXiv:2609.11975](https://arxiv.org/abs/2609.11975)). Built only from the public paper, including Supplementary Tables S1–S3.

Open `index.html` (or the GitHub Pages site of this repository) and press **▶ Tour** for an 8-stop guided story:
Space / → next, ← back, Esc exit; `#tour=N` links straight to a stop.

## How to read the map
| On the map | Meaning |
| :--- | :--- |
| **Districts** (south → north) | The paper's own Figure 1: 1 · the population, 2 · the design space, 3 · the theory on trial, 4 · papers ↔ code — each labelled with its thesis |
| 🏢 **Skyscraper** | A repository or agent system from the studied ecosystem |
| ⛪ **Cathedral** | The study's corpora and knowledge: registries, lineages, the pattern compendium |
| 🔭 **Observatory** | The study's instruments: coding, checks, audits, scores |
| 📡 **TV tower** | Intake channels through which records entered the registry |
| Scaffolding / ghost | Partly fills the empty cell (2 of 3 clauses) / does not work or has no code |
| 🎯 **Targets R1–R6** | Candidate regularities; pin colour = verdict, green arcs = supporting evidence, red arcs = counterevidence |
| ▦ **Plazas** | Tables painted on the ground: the design space (judge × selection signal) and Table 7's cost × ambition matrix with rules (a)/(b) |
| Weather, traffic, queues | Limitations drawn on the finding they weaken |

Alt/Option + scroll (or `[` / `]`) resizes buildings.

## Contents
| Path | What |
| :--- | :--- |
| `index.html`, `city-data.js` | Static MapLibre viewer (no build step; loads MapLibre and fonts from CDNs) |
| `spec/01-domain-profile.yaml` | Discovery-stage profile |
| `spec/02-city-spec.json` | Semantic city specification the viewer is compiled from |

Generated with [Metropolis-Kit](https://github.com/omniscale-ai/metropolis-kit) (`examples/autoresearch-wild/`):
```bash
python3 -m cli.compiler --spec examples/autoresearch-wild/02-city-spec.json --web-dir ../ai-research-bench/
```
