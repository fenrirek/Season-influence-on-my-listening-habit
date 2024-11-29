# Season-influence-on-my-listening-habit
Analyzing the effect of seasons on music preferences using Spotify, AccuWeather and Genius API.

## Project Overview

This project explores how seasons and weather conditions influence my music listening habits. By analyzing my Spotify listening history, weather data from AccuWeather, and sentiment analysis of lyrics, the goal is to uncover patterns in music preferences such as genres, tempos, and moods across seasons.

---

## 📂 **Dataset**
### **Spotify Listening History**
- **Source**: Spotify
- **Description**: This dataset contains information about the tracks I've listened to, including:
  - **Track Name**: The title of the song.
  - **Artist**: The artist or band of the song.
  - **Played At**: Timestamp of when the track was played.

### **Weather Data**
- **Source**: AccuWeather API.
- **Description**:
  - Weather data will be fetched using the AccuWeather API, providing insights into the conditions during my listening sessions.
  - Attributes included:
    - **Temperature**: Ambient temperature at the time of listening.
    - **Humidity**: Percentage humidity in the air.
    - **Weather Type**: Conditions like sunny, cloudy, or rainy.
    - **Location**: Retrieved using AccuWeather’s location services.
  - Weather information will be aligned with Spotify data using the `Played At` timestamp.

### **Sentiment Analysis of Lyrics**
- **Source**: Lyrics fetched using the Genius API.
- **Description**:
  - Sentiment analysis will be performed on the lyrics to classify emotional tone (e.g., positive, neutral, negative).
  - Examples of extracted features:
    - Sentiment score (polarity of lyrics: positive, neutral, or negative).
    - Emotion categories (happiness, sadness, etc.).
  - Lyrics sentiment will be aligned with Spotify data to analyze patterns by weather conditions and seasons.

### **Combined Dataset**
- The dataset integrates Spotify listening history, weather data, and sentiment analysis results, with columns like::
  - `Track Name`, `Artist`, `Played At`, `Sentiment Score`, `Season`, `Weather Type`, `Temperature`, `Humidity`.

---

## 🛠️ **Plan**

### **Data Collection**
1. **Spotify Data**:
   - Fetch listening history using the Spotify (`user-read-recently-played` scope).
   - Enrich the dataset with audio features using the `audio-features` endpoint.
2. **Weather Data**:
   - Fetch weather data using the AccuWeather API.
   - Steps:
     - Use the Geoposition API to retrieve `locationKey` based on my location.
     - Use the `locationKey` to fetch current weather conditions.
   - Align weather data with Spotify tracks based on the `Played At` timestamp.
3. **Lyrics Data**:
   - Retrieve lyrics using the Genius API and align them with Spotify tracks.

### **Exploratory Data Analysis (EDA)**
- I aim to analyze:
  - Music preferences by season (e.g., genres, tempos, moods in summer vs. winter).
  - Trends in tempo, mood, and energy across months grouped by seasons.
  - Trends in sentiment scores and genres across seasons.

### **Visualization**
- I will try to uncover patterns and relationships between seasons and music preferences. Through visualizations such as bar charts, line graphs, and scatter plots, the analysis highlights trends in genres, tempos, and moods based on seasons.

### **Sentiment Analysis**
- Perform sentiment analysis on the lyrics to extract emotional tone and sentiment scores.
- Align sentiment features with weather data to identify emotional trends.

### **Machine Learning**
- If possible, I aim to build a classification model to predict whether I would listen to a song in specific weather conditions or seasons:
- **Features**: Sentiment scores, genres, tempos, weather data.
- **Target Variable**: `Listen (Yes/No)` based on weather and season.
- **Techniques**:
  - Logistic Regression, Random Forest Classifier, Gradient Boosting.

---
