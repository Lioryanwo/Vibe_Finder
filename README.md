# VibeFinder – Personalized Song Prediction

## 🎵 Project Overview
VibeFinder is a machine learning project designed to predict which songs a user is most likely to enjoy, using real music data from the Spotify Web API.  
The system analyzes audio features, listening history, and user behavior patterns to generate accurate and personalized song recommendations.

---

## 🎯 Problem Definition
With millions of tracks available on streaming platforms, users often struggle to discover new music that truly matches their personal taste.  
While Spotify provides recommendation playlists, they may not always reflect each user's unique preferences.

**This project defines the prediction task as follows:**

- **Input:**  
  - User’s Top Tracks  
  - Recently Played Tracks  
  - Audio Features (energy, valence, tempo, danceability, etc.)

- **Output:**  
  - A ranked list of recommended songs  
  - A match/similarity score for each track

---

## 📊 Data Sources
All data is retrieved directly from:

### ✔️ Spotify Web API
- Audio Features  
- Track Metadata  
- Listening History  
- Artist and Genre Information  

**No manual labeling is required — the API provides rich, structured data.**

---

## 🧠 Planned Models and Methods
- **Baseline Models:**  
  - Decision tree
  - K-Nearest Neighbors (KNN)

- **Advanced Models (next stages):**  
  - XGBoost  
  - Neural Networks  
  - Hybrid recommendation models

---

## 📏 Evaluation Metrics
The system’s performance will be evaluated based on:

- **Precision** – Proportion of relevant recommended songs  
- **Recall** – Ability to recover songs the user actually likes  
- **Hit Ratio** – Whether at least one recommendation matches the user’s taste  
- **Future**: User feedback / qualitative evaluation

---

## 📁 Repository Structure
