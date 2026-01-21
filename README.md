# Spotify Song Clustering and Recommendation

**Author:** Hilal Işık  
*This project was completed when the Spotify API allowed full access to song features and metadata (around 2019–2021). Some endpoints used may have changed or require updated authentication today.*

---

## Project Overview

This project uses the **Spotify API** and **Billboard Hot 100 data** to analyze and cluster popular songs, and then provide **song recommendations** based on user preferences.  

The workflow included:

1. Collecting **top songs** from Billboard and Spotify (initially 1000 songs, later 5000).  
2. Using **classical ML clustering (KMeans)** to group songs by audio features.  
3. Creating a **simple recommendation system**:  
   - If a user’s favorite song is in the top 100, recommend another top 100 song randomly.  
   - If not, recommend a song from the **same cluster** using Spotify features.  

> Note: The project was completed before certain Spotify API restrictions. Today, some endpoints may require **updated authentication or paid plans**.

---

## Project Steps

### Data Collection

- **Spotify API:** Collected audio features (tempo, energy, danceability, etc.) for songs.  
- **Billboard Hot 100:** Scraped the top 100 songs from [Billboard](https://www.billboard.com/charts/hot-100/).  
- Combined the data into a **Pandas DataFrame** for analysis.

---

### Data Preparation

- Cleaned and standardized song features  
- Removed duplicates and missing values  
- Scaled numerical features using `StandardScaler` from `sklearn`

---

### Clustering with KMeans

- Used **Elbow Method** to determine optimal number of clusters  
- Applied **KMeans clustering** to group songs based on features  
- Evaluated clusters using **silhouette scores**  

---

### Recommendation System

- Created a **Python function** to interact with the user:  
  - User inputs their favorite song  
  - If the song is in **top 100**, randomly recommend another top song  
  - If not, find the **cluster of the song** and recommend another song from that cluster  

---

## Tools and Libraries

- **Data Manipulation:** `pandas`, `numpy`  
- **Web Scraping:** `BeautifulSoup`, `requests`  
- **Machine Learning:** `scikit-learn` (`KMeans`, `StandardScaler`, `silhouette_score`)  
- **Spotify API:** `spotipy` with `SpotifyClientCredentials`  
- **Visualization:** `matplotlib`  
- **Persistence:** `pickle`, `json`  

---

## Outcome

- Created **clusters of popular songs** based on Spotify audio features.  
- Built a **simple recommendation system** for users based on their favorite songs.  
- Demonstrated practical **web scraping, data preprocessing, clustering, and API integration**.

---

## Notes

- Some Spotify API endpoints used in this project **may have changed**; today, authentication may require a **Spotify Developer account**.  
- This project is a **learning and exploration exercise**, combining classical ML with real-world music data.

---

## License

**MIT License**

