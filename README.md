# Spotify---Recommender-System
A user profile based Spotify Recommender System.

# Spotify User Data Analysis & Recommendation Toolkit

This project provides a comprehensive toolkit for analyzing Spotify user data, enriching track features, generating ranked recommendations, and adaptively learning from user feedback using a multi-source strategy.

---

## 🔧 Modules & Features

### 1. **HelperFunctions**
- Validate and refresh Spotify access tokens.
- Convert nested `defaultdict` structures for JSON serialization.
- Apply exponential time decay to event timestamps.
- Build user preference vectors from track features.
- Print formatted song metadata.

### 2. **SpotifyDataEnricher**
- Enriches a DataFrame of Spotify track IDs using the Spotify API.
- Adds missing metadata and audio features.
- Handles API rate limiting and retries.
- Ensures consistency across all relevant metadata fields.

### 3. **SpotifyUserDataFetcher**
- Fetches and scores user-related data from Spotify:
  - Top tracks
  - Recently played tracks
  - Saved tracks
  - Tracks from top artists
- Combines data sources using configurable weights.
- Outputs a ranked list of tracks based on aggregated user preferences.

### 4. **EpsilonGreedyBandit**
- Implements an epsilon-greedy algorithm for adaptive source selection.
- Balances exploration (random source selection) and exploitation (best-performing source).
- Dynamically updates source weights based on feedback.

### 5. **RecommendationFeedbackCollector**
- Generates recommendations using a FAISS index and user profile vectors.
- Prompts the user for feedback on each source’s recommendations.
- Collects and structures ratings to refine future source weights or models.

---

