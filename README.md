# 📊 YouTube Data Analytics

A Python-based data analytics project that fetches the **most popular YouTube videos in India** using the YouTube Data API v3, analyzes the data using SQL queries and Pandas, and visualizes insights with Matplotlib.

---

## 🔍 What It Does

1. **Fetches Live Data** — Pulls the top trending YouTube videos in India (`regionCode=IN`) via the YouTube Data API v3, including title, channel, views, and likes.
2. **Stores Raw Data** — Saves the fetched video data locally as `youtube_raw.json`.
3. **Cleans & Analyzes** — Loads data into a Pandas DataFrame, converts numeric columns, and runs SQL queries using `pandasql`.
4. **Visualizes Results** — Generates a pie chart and a horizontal bar chart using Matplotlib.

---

## 📈 Analytics & SQL Queries

| Query | Description |
|---|---|
| `result` | Top 10 videos ordered by **likes** (descending) |
| `result_likes` | Top 10 videos ordered by **likes** (ascending) |
| `result_both` | Top 10 videos ordered by **likes & views** (descending) |
| `result_engagement` | Top 10 videos by **engagement rate** (`likes / views * 100`) |

---

## 📊 Visualizations

- **`youtube_piechart.png`** — Pie chart of the top 10 channels by total views
- **`youtube_barchart.png`** — Horizontal bar chart of the top 10 videos by view count

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.13 | Core language |
| YouTube Data API v3 | Fetch trending video data |
| `google-api-python-client` | API client library |
| Pandas | DataFrame creation & data cleaning |
| pandasql | Run SQL queries on DataFrames |
| Matplotlib | Charts & visualizations |
| JSON | Raw data storage |

---

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/youtube-data-analytics.git
cd youtube-data-analytics
```

### 2. Install dependencies

```bash
pip install google-api-python-client pandas pandasql matplotlib seaborn
```

---

## 🔑 API Key Setup

1. Go to the [Google Cloud Console](https://console.cloud.google.com/)
2. Create a project and enable the **YouTube Data API v3**
3. Generate an API key
4. In the notebook, replace the placeholder with your key:

```python
API_KEY = "your_api_key_here"
---

## ▶️ Usage

Open and run the Jupyter Notebook cell by cell:

```bash
jupyter notebook youtube_data_analytics.ipynb
```

### Notebook Flow

```
Install API client
       ↓
Build YouTube API connection
       ↓
Fetch top 500 trending videos (India)
       ↓
Parse → Save to youtube_raw.json
       ↓
Load into Pandas DataFrame
       ↓
Clean data (convert views & likes to numeric)
       ↓
SQL queries with pandasql
       ↓
Visualize with Matplotlib
```

---

## 📁 Output Files

| File | Description |
|---|---|
| `youtube_raw.json` | Raw video data fetched from the API |
| `youtube_piechart.png` | Pie chart — top 10 channels by views |
| `youtube_barchart.png` | Bar chart — top 10 videos by views |

---

## 📋 Requirements

- Python 3.8+
- Jupyter Notebook or JupyterLab
- A valid YouTube Data API v3 key

---

## ⚠️ Disclaimer

This project uses the YouTube Data API v3 and is subject to [Google's API Terms of Service](https://developers.google.com/youtube/terms/api-services-terms-of-service). API usage is subject to daily quota limits.

---

## 📄 License

This project is licensed under the MIT License.
