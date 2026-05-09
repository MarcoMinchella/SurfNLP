# RAG for Surfing Spot Reviews

## Project Overview

This project explores how **Retrieval-Augmented Generation (RAG)** can be applied to a niche domain: surfing spot reviews. Using a dataset of ~2,000 user reviews from TripAdvisor, Google Maps, and Yelp, covering 21 popular surfing beaches worldwide, we demonstrate how RAG can help answer nuanced questions about surf conditions, atmosphere, facilities, and overall experiences.

The project is implemented entirely in a Python Jupyter Notebook, making it easy to follow along, experiment with, and extend.

-----

## Dataset

- **Sources:** TripAdvisor, Google Maps, Yelp
- **Size:** ~2,000 reviews
- **Coverage:** 21 surfing beaches, varied by location, wave quality, and popularity
- **Content:** User-generated text reviews, capturing experiences such as:
  - Wave difficulty and surf quality
  - Safety and crowd levels
  - Local amenities (restaurants, rentals, schools)
  - Atmosphere and community

-----

## Repository Structure

```
.
├── data/                                  # All review data
│   ├── NewCSVTagged_NLP/                  # Tagged/processed reviews
│   ├── NewCSV_NLP/                        # Cleaned reviews
│   ├── AllReviews.csv                     # Combined dataset
│   └── *.csv                              # One file per surfing spot
├── Milliaud_Minchella_NLP_Part2.ipynb     # Main notebook (RAG pipeline + experiments)
├── milliaud_minchella_nlp_part2.py        # Standalone Python version
└── README.md
```

-----

## Methodology

**1. Preprocessing**

- Cleaning text, removing duplicates, and translating all reviews into English.
- Splitting reviews into manageable chunks for retrieval.

**2. Embedding & Indexing**

- Reviews are embedded into vector space using modern sentence embeddings.
- Indexed with **FAISS** for efficient similarity search.

**3. RAG Pipeline**

- **Retriever:** fetches the most relevant reviews for a query.
- **Generator:** uses an LLM to synthesize natural-language answers grounded in the retrieved reviews.

**4. Exploration via Notebook**

- Full code walkthrough in Jupyter Notebook format.
- Example queries:
  - *“What’s a good surf spot in winter?”*
  - *“What is a good spot for beginners?”*
  - *“What’s a good spot for confirmed-level surfers?”*