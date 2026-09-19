# recommendation_system

A modular, terminal-based text search and recommendation engine built entirely in **Python** without relying on external machine learning or AI libraries (like scikit-learn). This project uses pure mathematical logic and text preprocessing to vector-match user queries with a book dataset.

## Features
* **Built From Scratch:** Implemented the complete TF-IDF algorithmic logic and vector comparison calculations independently.
* **Text Preprocessing Pipeline:** Cleans text, tokenizes words, and filters out common stop-words dynamically.
* **Vector-Based Matching:** Uses Cosine Similarity to calculate the geometric angle between query vectors and document vectors, outputting ranked recommendations.
* **Memory-Optimized Testing:** Features a lightweight framework using a smaller dataset version (`small_data.csv`) to minimize memory overhead and speed up testing cycles compared to the full `books.csv`.
* **Interactive CLI:** Includes a clean, user-friendly terminal menu for typing queries and reviewing ranked recommendations.

## Project Structure
* `main.py` – Controls the interactive console menu, handles the primary TF-IDF matrix calculations, and coordinates the recommendation flow.
* `preprocessing.py` – Contains helper functions for string cleaning, word tokenization, and stop-word filtering.
* `small_data.csv` – A lightweight dataset containing a downscaled sample of tabular book details for fast debugging and development.
* `books.csv` – The full-scale dataset housing the entire library database.

## How It Works
1. **Data Cleaning:** The engine reads text attributes from the CSV dataset and passes them through `preprocessing.py` to extract pure semantic tokens.
2. **TF-IDF Matrix Construction:** The application calculates the Term Frequency (TF) and Inverse Document Frequency (IDF) variables manually to convert text descriptions into mathematical weight vectors.
3. **Query Evaluation & Ranking:** When a user types a query, it is converted into the same vector space. The engine calculates the **Cosine Similarity** score between the query vector and all text profiles, sorting the dataset to display the most relevant matches instantly.
