# Challengers Player Analytics

A lightweight, offline-friendly analytics dashboard for exploring competitive Call of Duty Challengers player performance.

## Overview

Challengers Player Analytics is a fan-built player-performance explorer for scouting and comparison. Rather than presenting a raw stat table, it combines interactive field views, rankings, filters, and player-level drilldowns to make the local dataset easier to investigate.

## Features

- Interactive player scatter plots with selectable metrics and field-average reference lines
- Leaderboard and ranking views with Top 10, Top 20, and full-field options
- Searchable, filterable, sortable player table with overall and game-mode metric views
- Player detail drawer with a BUSHAI Summary and sample-size context
- Relative Performance Profile radar using dataset percentiles and derived composites
- Player-versus-field and player-versus-player percentile comparisons
- Hardpoint, Search & Destroy, and Control breakdowns
- Distribution and quadrant analysis views
- Local, responsive interface that works directly from `file://`

## Screenshots

> Screenshots coming soon.

## Running Locally

This project intentionally requires no Node.js, npm, backend, build process, or local development server.

Clone or download this repository, then open `index.html` in a modern browser. It is designed to run directly from `file://`.

```bash
git clone <repository-url>
```

If you do not use Git, download the repository ZIP, extract it, and double-click `index.html`.

## Project Structure

```text
.
├── index.html                         # Application shell, footer, and About dialog
├── about.html                         # Local About & Attribution page
├── styles.css                         # Main visual styling
├── styles-extra.css                   # Supporting UI styling
├── app.js                             # Filters, analytics, drawer, and ECharts rendering
├── data.js                            # Locally bundled player dataset used at runtime
├── breakingpoint_challengers_2024_stats.csv  # Source CSV snapshot
├── generate-data.ps1                  # Build-time CSV-to-data.js helper
├── logo1.jpg
├── logo2.jpeg
├── lib/
│   └── echarts.min.js                 # Local Apache ECharts distribution
├── LICENSE
├── THIRD_PARTY_NOTICES.md
└── README.md
```

## Data & Analytics

### Source statistics

The locally bundled dataset contains player statistics originating from publicly accessible statistics on [BreakingPoint.gg](https://breakingpoint.gg/), including kills, deaths, K/D, BP Rating, Slayer Rating, Hardpoint statistics, Search & Destroy statistics, and Control statistics.

### Derived analytics

This project independently calculates dataset percentiles, relative performance profiles, composite mode indicators, quadrant analysis, visual rankings, player comparisons, and the BUSHAI Summary. Derived analytics are independently calculated by this project and are not official Breaking Point metrics.

## How Percentiles Work

Percentile scores compare a player’s metric against the other players represented in the local dataset. A player shown in the 90th percentile for K/D ranks at or above approximately 90% of the players represented here for that metric.

Results reflect only the players and samples represented by this dataset. They are context tools for exploration, not an official competitive ranking system.

## Tech Stack

- HTML5
- CSS
- Vanilla JavaScript
- [Apache ECharts](https://echarts.apache.org/)

The application is intentionally static and dependency-light so it can run directly from a local file without a build process or server.

## Why Offline?

The local approach makes the dashboard easy to share with coaches or analysts, requires no account or server, and keeps the charts and player data bundled with the project. The application makes no runtime API calls and does not upload data.

## Disclaimer & Data Attribution

This is an independent, non-commercial fan project and is not affiliated with, endorsed by, sponsored by, or operated by Breaking Point Media Inc.

Certain underlying Call of Duty player statistics displayed by this project were obtained from publicly accessible pages on [BreakingPoint.gg](https://breakingpoint.gg/).

Breaking Point, BreakingPoint.gg, and related names, trademarks, content, and data remain the property of their respective owners.

Any analytics created by this project — including percentiles, comparisons, composite ratings, radar profiles, visualizations, and other derived analysis — are independently calculated and should not be interpreted as official Breaking Point statistics. The in-app [About & Attribution page](about.html) presents the same information in a concise, reader-friendly format.

## Licensing

The original software source code in this repository is licensed under the MIT License found in the [`LICENSE`](LICENSE) file.

The MIT License applies only to original software created for this project. It does not grant rights to third-party data, trademarks, logos, content, or other intellectual property originating from Breaking Point or other third parties.

This project uses [Apache ECharts](https://echarts.apache.org/), which is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0). See [`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md) for attribution and notice information.

## Contributing

Suggestions, bug reports, and improvements are welcome. If submitting changes, please keep the project:

- Static
- Dependency-light
- Offline-friendly
- Focused on useful player analytics

## Project Status

This is a fan project and may evolve as I experiment with better ways to visualize competitive player performance.
