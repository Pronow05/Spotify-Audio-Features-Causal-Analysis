# Spotify-Audio-Features-Causal-Analysis
This project analyzes the causal relationships between audio features and the popularity of Spotify tracks using the Spotify Dataset (1921–2020). By leveraging a dataset of over 600,000 tracks and applying exploratory data analysis and causal inference techniques, the project uncovers how audio features such as energy, danceability, acousticness, tempo, and liveness influence track popularity.

## Dataset 
  - Name: Spotify Dataset 1921–2020
  - Source: Kaggle - Spotify Dataset 1921-2020
  - Size: ~600,000 tracks
  - Key Features:
    - `popularity`: A score (0–100) representing a track's popularity.
    - `danceability`: How suitable a track is for dancing.
    - `energy`: Perceptual measure of intensity and activity.
    - `tempo`: Overall tempo of a track (BPM).
    - `acousticness`: Confidence measure of a track being acoustic.
    - `liveness`: Presence of a live audience in the recording.
    - `release_date`: Date of track release.
    - `explicit`: Binary indicator of explicit content.
    - `valence`: Musical positiveness conveyed by the track.
    - `loudness`: Average loudness of a track in decibels.

## Objectives
  1. Explore temporal and feature-based trends in music attributes.
  2. Investigate relationships between audio features and popularity.
  3. Apply causal inference to uncover causal relationships between:
    - energy and popularity
    - liveness and popularity
    - danceability and popularity
    - tempo and popularity
    - acousticness and popularity

## Tools and Libraries
  - Programming Language: Python
  - Libraries:
    - Data Manipulation: Pandas, NumPy
    - Visualization: Matplotlib, Seaborn
    - Causal Inference: DoWhy, EconML
    - Preprocessing: sklearn

## Implementation Steps
### 1. Data Loading and Cleaning
  - Loaded the dataset and parsed release_date to extract the year.
  - Removed invalid or missing data.
  - Normalized audio features to ensure uniform scaling for analysis.
### 2. Exploratory Data Analysis (EDA)
  - Correlation Analysis: Visualized feature correlations with a heatmap.
  - Feature Distributions: Analyzed distributions of key audio features (danceability, energy, etc.).
  - Temporal Trends: Explored how attributes evolved over decades (e.g., decline in acousticness, rise in energy).
  - Popularity Trends: Examined relationships between year, energy, and popularity.
### 3. Causal Inference
  - Defined treatment (energy, danceability, etc.), outcome (popularity), and confounders (release_year, explicit, valence, etc.).
  - Used DoWhy to:
    - Construct causal graphs.
    - Estimate average treatment effects (ATE) for each feature.
    - Validate results with refutation tests (e.g., placebo treatment, subset refuter).
  - Visualized causal estimates for comparison.
### 4. Key Findings
  - Energy: Tracks with higher energy levels are generally more popular.
  - Danceability: Danceable tracks are likely to gain higher popularity scores.
  - Acousticness: Lower acousticness correlates with higher popularity, aligning with trends in mainstream genres like EDM and hip-hop.
  - Tempo: Moderate tempos appear more favorable for popularity.
  - Liveness: Limited impact on popularity, except for exceptionally popular tracks.
