# Book Recommendation Model using RAG

This project implements a book recommendation system using Retrieval-Augmented Generation (RAG) architecture. The model is built with the Groq API and LangChain, leveraging Amazon books data to provide personalized book recommendations. The RAG model combines the strengths of retrieval and generation, allowing it to generate contextually relevant recommendations based on user queries.

## Data

The model uses Amazon books data from [Kaggle](https://www.kaggle.com/datasets/mohamedbakhet/amazon-books-reviews?select=books_data.csv). It contains metdata of book and reviews tables joined by `Tilte` column. The data has been cleaned by dropping and replacing relevant Nan values. Converting to the required datatypes based on the column information. And finally aggregating customers reviews data by transforming columns using mean and concatenation processes. Final data used is present in `transformed_df.csv`.

## Installation

To set up the project locally, follow these steps:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/book-recommendation-rag.git
   cd book-recommendation-rag
   ```

2. **Install required packages:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables:**
   
   Create a `.env` file in the root directory and add your Groq API key:

   ```plaintext
   GROQ_API_KEY="your_groq_api_key"
   ```

## Usage

To run the model and get book recommendations, execute the following command:

```bash
python book_recommendation_RAG.py
```

### Example Query

```plaintext
Suggest a book by Thomas Hardy with a rating of 4.5 and above in genre drama.
```

The model will return a list of recommended books based on the query.

