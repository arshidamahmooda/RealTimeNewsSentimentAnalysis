

````markdown
# Real-Time News Sentiment Dashboard

This project is a **real-time news sentiment classification and visualization dashboard**. It fetches the latest news headlines from **NewsAPI** (with **GNews** fallback), classifies each headline as **Positive** or **Negative**, and visualizes the results in a Streamlit dashboard.

---

## Features

- Fetch real-time news from **NewsAPI** or **GNews**.
- Classify headlines as **Positive** or **Negative** using **TextBlob**.
- Store predictions in **Parquet** files for history tracking.
- Visualize:
  - Latest headlines with sentiment.
  - Sentiment distribution (bar chart).
  - Positive sentiment trend over time (line chart).
- Fully deployable on **Streamlit Cloud**.

---

## Requirements

Python 3.9+ with the following packages:

```bash
streamlit
pandas
plotly
textblob
gnews
requests
pyarrow
````

You can install dependencies using:

```bash
pip install -r requirements.txt
```

---

## Setup

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/repo-name.git
cd repo-name
```

2. **Add your NewsAPI key**

Open `app.py` and replace:

```python
NEWSAPI_KEY = "YOUR_NEWSAPI_KEY"
```

with your actual NewsAPI key.

> You can get a free key from [https://newsapi.org](https://newsapi.org).

3. **Run locally**

```bash
streamlit run app.py
```

4. **Optional: Deploy on Streamlit Cloud**

* Push your repository to GitHub.
* Go to [https://share.streamlit.io](https://share.streamlit.io) and connect your repo.
* Set `app.py` as the main file.

---

## Usage

* Open the dashboard.
* Click **Fetch & Classify Latest News** to load the latest headlines.
* Use the sidebar slider to set **refresh interval** (in seconds).
* View:

  * Latest headlines with sentiment.
  * Sentiment distribution bar chart.
  * Positive sentiment trend line chart.

---

## Project Structure

```
├── app.py                # Streamlit app
├── predictions_parquet/  # Folder to store prediction history (Parquet files)
├── requirements.txt      # Python dependencies
└── README.md             # Project description and instructions
```

---

## Notes

* If NewsAPI fails (due to invalid key or rate limits), the app automatically uses **GNews** as a fallback.
* The sentiment classification uses **TextBlob**, which is lightweight and deployable on Streamlit Cloud.
* The dashboard updates predictions in real-time and keeps historical data in Parquet files.

---

## Screenshots

*(Add screenshots of your Streamlit dashboard here)*

---

## License

MIT License

```
