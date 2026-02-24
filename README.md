# 🎬 The Popularity Paradox
## Why the Most Viewed YouTube Categories Aren't the Most Appreciated

> *"A video with 500 million views sounds like a clear success. But does that really mean people loved it?"*

---

## 📌 The Question

On YouTube, does **popularity** actually mean **appreciation**?

Views measure how many people clicked — not how they felt. This project explores whether the most-viewed YouTube categories are actually the ones that earn the most genuine engagement from their audiences.

---

## 📁 Project Structure

```
YouTube_Popularity_Paradox/
│
├── README.md                              ← You are here
├── YouTube_Popularity_Paradox_FINAL.ipynb ← Main analysis notebook
├── youtube.csv                            ← Dataset (from Kaggle)
└── presentation.html                      ← Visual data story
```

---

## 📊 Dataset

| Detail | Info |
|--------|------|
| Source | [YouTube Trending Dataset — Kaggle](https://www.kaggle.com/) |
| Size | 161,470 trending videos |
| Countries | Multiple |
| Categories | 15 |
| Key columns | views, likes, comment_count, category_id |

---

## 🔧 Tools Used

| Tool | Purpose |
|------|---------|
| Python 3 | Core language |
| Pandas | Data loading, cleaning, grouping |
| Matplotlib | Bar charts and viral paradox chart |
| Seaborn | Engagement heatmap |
| Google Colab | Notebook environment |

---

## 📐 Metric Created: `like_ratio`

```python
like_ratio = likes / views
```

Since views alone don't measure appreciation, I created `like_ratio` — the percentage of viewers who actively liked a video. A score of 0.05 means 5 out of every 100 viewers liked it.

I also created:
- `comment_ratio` = comments / views
- `engagement_score` = like_ratio + comment_ratio

---

## 🔍 Key Findings

### Finding 1 — The Rankings Flip Completely
The most-viewed categories are **not** the most appreciated:

| Rank by Views | Category | Rank by Like Ratio |
|---|---|---|
| #1 | Music (8.2M avg views) | #5 |
| #7 | Comedy | **#1 (5.23%)** |
| #11 | Howto & Style | **#2 (5.09%)** |

### Finding 2 — The Viral Paradox 🔍
Videos with **100M+ views** have a like ratio **57% lower** than videos under 100K views:

| View Range | Like Ratio |
|---|---|
| Under 100K | 4.03% |
| 1M – 10M | 3.59% |
| **Over 100M** | **1.73%** |

### Finding 3 — Niche Communities Win
Gaming, Education, and Comedy audiences are more loyal and more engaged per viewer despite having fewer total views.

---

## 🏁 Conclusion

> **On YouTube, popularity is loud. Appreciation is honest.**

The data across 161,470 videos shows that reach and resonance are two different things — and chasing raw view counts may be exactly the wrong strategy for building a loyal audience.

---

## ⚠️ Limitations

- Dataset covers **trending videos only** — not all YouTube content
- Engagement may vary by culture, language, and algorithm behavior
- Results show **correlation, not causation**

---

## 🏆 Submission

**Challenge:** Codédex February 2026 Dataset Challenge  
**Category:** Data Science / Data Analysis  
**Date:** February 2026
