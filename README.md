📌 Project Overview

This project explores how Retrieval-Augmented Generation (RAG) can be applied to a niche domain: surfing spot reviews. Using a dataset of ~2000 user reviews from TripAdvisor, Google Maps, and Yelp, covering 21 popular surfing beaches worldwide, we demonstrate how RAG can help answer nuanced questions about surf conditions, atmosphere, facilities, and overall experiences.

The project is implemented entirely in a Python Jupyter Notebook, making it easy to follow along, experiment, and extend.

🏄 Dataset

Sources: TripAdvisor, Google Maps, Yelp

Size: ~2000 reviews

Coverage: 21 surfing beaches (varied by location, wave quality, and popularity)

Content: User-generated text reviews, capturing experiences such as:

Wave difficulty & surf quality

Safety & crowd levels

Local amenities (restaurants, rentals, schools)

Atmosphere & community

⚙️ Methodology

Preprocessing

Cleaning text, removing duplicates and translating all reviews in english language.

Splitting reviews into manageable chunks for retrieval.

Embedding & Indexing

Reviews are embedded into vector space using modern sentence embeddings.

Indexed with FAISS for efficient similarity search.

RAG Pipeline

Retriever: Fetches the most relevant reviews for a query.

Generator: Uses an LLM to synthesize natural-language answers grounded in retrieved reviews.

Exploration via Notebook

Code walkthrough in Jupyter Notebook format.

Example queries like:

“What's a good surf spot in winter ?”

“What is a good spot for beginners ?”

“What's a good spot for confirmed level surfers ?”
