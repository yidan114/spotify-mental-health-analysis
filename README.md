# Are We Listening to Sadder Music?

A data-driven look at what 586,672 Spotify tracks reveal about our collective mood — and whether the music we choose says something about how we're really doing.

## Why This Project

Depression prevalence in the U.S. has climbed steadily over the past decade. Meanwhile, the songs topping our playlists have been getting quieter, slower, and measurably less "happy" by Spotify's own metrics. Coincidence, or are we unconsciously reaching for music that mirrors what we feel but can't always articulate?

This project doesn't pretend to answer that. But it maps out the terrain — where the numbers converge, where they diverge, and where the question itself gets interesting.

## What I Found

The average valence (Spotify's measure of musical positivity) dropped from 0.537 to 0.503 after COVID hit. That gap is statistically significant (t = 18.13, p < 0.001) — not huge in absolute terms, but consistent and directional.

Valence and U.S. depression rates move in opposite directions (r = -0.570). As more Americans report depressive symptoms, the music that rises to the top skews darker. The pattern is sharper among popular tracks than across the full catalog, which suggests this isn't random noise — it's something about what listeners actively choose.

None of this proves causation. Music might reflect collective mood. It might shape it. It might just be that minor keys sound better in headphones on the subway. The data doesn't settle that debate, but it gives it a foundation.

## Data

- **Spotify Audio Features**: 586,672 tracks (1921–2021) via Kaggle, sourced from Spotify Web API. Key fields: valence, energy, danceability, mode, popularity.
- **U.S. Mental Health**: Depression and anxiety prevalence compiled from CDC (NHANES, NHIS, Household Pulse Survey).

## Methods

- Time-series analysis of audio features (2000–2021)
- Pearson correlation between annual valence and depression prevalence
- Welch's t-test: pre-COVID vs post-COVID valence
- Subgroup comparison: popular tracks vs full catalog

## Tools

Python · pandas · matplotlib · seaborn · scipy

## Structure

    ├── 01_data_exploration.ipynb
    ├── figures/
    ├── data/raw/                   (not tracked)
    ├── data/processed/
    └── README.md

## Author

**Yidan Kong** · QMSS, Columbia University
