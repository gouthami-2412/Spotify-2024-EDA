# Most Streamed Spotify Songs 2024 — Exploratory Data Analysis

An exploratory data analysis of the [Most Streamed Spotify Songs 2024](https://www.kaggle.com/datasets/nelgiriyewithana/most-streamed-spotify-songs-2024) dataset from Kaggle, covering cross-platform streaming performance (Spotify, YouTube, TikTok, Apple Music, Deezer, Pandora, Soundcloud, radio) for ~4,600 of the most-streamed tracks.

## Author

Gogineni Gouthami — B.Tech CSE, IIITDM Kancheepuram

## Project Goal

Rather than just describing individual columns, this EDA is built around specific investigative questions:

1. How trustworthy is this data, and what has to be fixed before it can be relied on?
2. Is streaming success concentrated in a few artists/tracks, or spread across many?
3. What correlates most strongly with a song's success — and does it hold across platforms?
4. Does going viral on TikTok actually translate into Spotify streams?
5. Does explicit content help, hurt, or make no real difference to performance?
6. Is chart position mostly about being old, or can new songs break through fast?
7. Are there tracks that are massive on one platform but nearly invisible on another?

## Key Findings

- **Data required real cleaning:** wrong file encoding, numbers stored as comma-separated text, and a couple of genuine duplicate rows had to be fixed before any analysis was possible.
- **Streaming success is highly concentrated:** a small number of artists account for a disproportionate share of total streams.
- **Playlist placement correlates most strongly with Spotify Streams** (~0.8), though this is correlation, not confirmed causation — the dataset is a single snapshot with no timeline.
- **TikTok virality does not reliably predict Spotify success** — the two are only weakly correlated, even after adjusting for number of TikTok posts.
- **Explicit content makes no meaningful difference to streaming performance.** Explicit content makes little difference to streaming performance — median streams were close between explicit and non-explicit tracks.
- **Older songs have a cumulative streaming advantage**, but the actual Top 100 all-time ranks still include plenty of very recent releases.
- **Cross-platform mismatches are real:** tracks with the largest gap between their best and worst platform tend to be big on YouTube or TikTok but comparatively small on Spotify specifically.

## Tools Used

- Python
- pandas, numpy — data cleaning and analysis
- matplotlib, seaborn — visualization

## Repository Contents

| File | Description |
|---|---|
| `spotify_EDA_notebook.ipynb` | Full EDA notebook with code, plots, and written analysis |
| `Most_Streamed_Spotify_Songs_2024.csv` | Raw dataset (source: Kaggle) |

## How to Run

1. Clone this repository
2. Install dependencies: `pip install pandas numpy matplotlib seaborn`
3. Open `spotify_eda.ipynb` in Jupyter Notebook / JupyterLab / VS Code
4. Run all cells

## Limitations

- Several platform-specific columns (SiriusXM, Soundcloud, TIDAL) had heavy missing data, limiting depth of analysis for those platforms.
- The dataset only includes songs that were already successful enough to reach an all-time rank, so findings don't generalize to music that never gained traction.
- Correlation-based findings (e.g. playlist count vs. streams) describe association, not proven causation.
