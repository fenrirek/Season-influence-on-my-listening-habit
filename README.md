# Season-influence-on-my-listening-habit
Analyzing the effect of seasons on music preferences using Spotify and PrettyMIDI.

## Project Overview

This project explores the relationship between seasons and my music listening habits. By analyzing my Spotify listening history and enriching it with advanced audio features extracted using **PrettyMIDI**, the goal is to uncover how seasonal changes (winter, spring, summer, and fall) influence the type of music I listen to, including genres, tempos, and moods. Additionally, I aim to build predictive models to classify whether I would listen to a particular song in a specific season based on its audio features.

---

## 📂 **Dataset**
### **Spotify Listening History**
- **Source**: Spotify
- **Description**: This dataset contains information about the tracks I've listened to, including:
  - **Track Name**: The title of the song.
  - **Artist**: The artist or band of the song.
  - **Played At**: Timestamp of when the track was played.

### **Audio Feature Extraction with PrettyMIDI**
- **Source**: MIDI files corresponding to Spotify tracks.
- **Description**:
  - MIDI files are analyzed using the `PrettyMIDI` Python library to extract advanced musical features:
    - **Tempo**: Average tempo of the track.
    - **Key and Mode**: Harmonic content of the track.
    - **Pitch Class Distribution**: Distribution of pitches used in the track.

### **Seasonal Data**
- **Source**: Derived from timestamps in Spotify data.
- **Description**:
  - Seasons are assigned based on the month of the `Played At` timestamp:
    - **Winter**: December, January, February
    - **Spring**: March, April, May
    - **Summer**: June, July, August
    - **Fall**: September, October, November
  - Each track is labeled with its corresponding season.

### **Combined Dataset**
- The Spotify dataset is enriched with a `Season` column based on the `Played At` timestamp, creating a unified dataset with the following columns:
  - `Track Name`, `Artist`, `Played At`, `Tempo`, `Energy`, `Weather Type`, `Temperature`, `Humidity`, `Season`.

---

## 🛠️ **Plan**

### **Data Collection**
1. **Spotify Data**:
   - Fetch listening history using the Spotify Web API (`user-read-recently-played` scope).
   - Enrich the dataset with audio features using the `audio-features` endpoint.
2. **MIDI Features**:
   - Extract advanced features like `Tempo`, `Key`, and `Pitch Class Distribution` from MIDI files using PrettyMIDI.
3. **Seasonal Data**:
   - Categorize each track into a season (winter, spring, summer, fall) based on the month in the `Played At` timestamp.

### **Exploratory Data Analysis (EDA)**
- I aim to analyze:
  - Music preferences by season (e.g., genres, tempos, moods in summer vs. winter).
  - Trends in tempo, mood, and energy across months grouped by seasons.
  - Trends in PrettyMIDI features like tempo and pitch distribution across months grouped by seasons.

### **Visualization**
- I will try to uncover patterns and relationships between seasons and music preferences. Through visualizations such as bar charts, line graphs, and scatter plots, the analysis highlights trends in genres, tempos, and moods based on seasons.

### **Machine Learning**
- If possible, I will try to build predictive models:
  - Whether I would listen to a given song in a specific season based on its audio features.
  - **Features**: `Tempo`, `Key`, `Pitch Class Distribution`.
  - **Target Variable**: `Listen (Yes/No)` in a given season.
  - **Techniques**: Logistic Regression, Random Forest, or Gradient Boosting.

---
