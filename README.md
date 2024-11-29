# Weather-influence-on-my-listening-habit
Analyzing the effect of weather conditions on music preferences using Spotify and weather APIs.

## Project Overview

This project explores the relationship between weather conditions and my music listening habits. The goal is to analyze how weather variables (e.g., temperature, humidity, and weather types like rain or sunshine) influence the type of music I listen to, including genres, tempos, and moods. By combining my personal Spotify listening history with historical weather data, I aim to uncover patterns and trends that provide deeper insights into my music preferences.

---

## 📂 **Dataset**
### **Spotify Listening History**
- **Source**: Spotify
- **Description**: This dataset contains information about the tracks I've listened to, including:
  - **Track Name**: The title of the song.
  - **Artist**: The artist or band of the song.
  - **Played At**: Timestamp of when the track was played.
  - **Audio Features** : Tempo, energy, valence, and other features retrieved from Spotify's `audio-features` endpoint.

### **Weather Data**
- **Source**: OpenWeatherMap
- **Description**: Weather data corresponding to the listening history timestamps, including:
  - **Temperature**: Current temperature at the listening time.
  - **Humidity**: Humidity levels at the listening time.
  - **Weather Type**: Descriptions such as sunny, cloudy, or rainy.

### **Combined Dataset**
- The Spotify and weather datasets are merged based on the timestamps, creating a unified dataset with the following columns:
  - `Track Name`, `Artist`, `Played At`, `Tempo`, `Energy`, `Weather Type`, `Temperature`, `Humidity`.

---

## 🛠️ **Plan**
### **Data Collection**
1. **Spotify Data**:
   - Fetch listening history using the Spotify Web API (`user-read-recently-played` scope).
   - Enrich the dataset with audio features using the `audio-features` endpoint.
2. **Weather Data**:
   - Use the OpenWeatherMap API to fetch historical weather data for the listening timestamps.

### **Exploratory Data Analysis (EDA)**
- I aim to analyze:
  - Music preferences by weather type (e.g., sunny vs. rainy).
  - Trends in tempo, genre, or mood relative to weather conditions.

### **Visualization**
- I will try to uncover patterns and relationships between weather conditions and music preferences. Through visualizations such as bar charts, line graphs, and scatter plots, the analysis highlights trends in genres, tempos, and moods across different weather types (e.g., sunny, rainy, or cold).

### **Machine Learning**
- If possible, I will try to build predictive models:
  - Predict music features (e.g., tempo or genre) based on weather.
  - Techniques: Logistic Regression, Random Forest, or Linear Regression.

---
