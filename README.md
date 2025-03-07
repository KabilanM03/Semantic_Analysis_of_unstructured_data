Semantic-Analysis-of-unstructured-data
Purpose: To create a web-based search application that allows users to search for Myntra fashion products by querying their descriptions and other attributes.

Technology Stack:

Backend: Elasticsearch: A search engine used to store, index, and search product data. SentenceTransformers: A Python library for encoding search queries into vectors using pre-trained models. Frontend: Streamlit: A Python library for building interactive web applications. Core Components:

Elasticsearch Setup:

Connection: The application connects to an Elasticsearch instance using basic authentication and a CA certificate. Indexing: An index named all_products is created to store product information. Index Mapping: Defines the structure of the product data, including fields for product ID, name, brand, gender, price, number of images, description, primary color, and a dense vector for the description. Search Functionality:

Encoding Search Queries: Uses the all-mpnet-base-v2 model from SentenceTransformers to encode user search queries into vectors. k-NN Search: Performs a k-nearest neighbors search on the DescriptionVector field in Elasticsearch to find the most relevant products based on the encoded search query. Result Display: Returns and displays the product name and description for the top matching products. Streamlit Web Interface:

User Input: Users can enter search queries into a text input field. Search Button: Triggers the search function when clicked. Results Display: Displays the search results, including product names and descriptions, in a user-friendly format.

