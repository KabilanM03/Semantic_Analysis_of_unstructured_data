# **Semantic Analysis of Unstructured Data**
A web-based search application for querying **Myntra fashion products** based on descriptions and attributes.

---

## **1. Project Overview**
This project implements a **semantic search engine** that enables users to search for **fashion products** using **natural language queries**. The application is built using **Elasticsearch** for indexing and retrieval and **Streamlit** for an interactive web interface.

---

## **2. Technology Stack**
The system leverages the following technologies:

### **Backend**
- **Elasticsearch** – Stores, indexes, and retrieves product data.
- **SentenceTransformers** – Encodes search queries into vector representations using a **pre-trained deep learning model**.

### **Frontend**
- **Streamlit** – Provides an interactive web-based interface for searching fashion products.

---

## **3. Core Components**
The system consists of the following key modules:

### **Elasticsearch Setup**
- **Connection**: Establishes a secure connection to an **Elasticsearch instance** using **basic authentication** and a **CA certificate**.
- **Indexing**: Creates an index named `all_products` to store product information.
- **Index Mapping**: Defines the structure of product data, including:
  - **Product ID**
  - **Product Name**
  - **Brand**
  - **Gender**
  - **Price**
  - **Number of Images**
  - **Product Description**
  - **Primary Colour**
  - **Dense Vector Representation** (for similarity search)

---

### **Search Functionality**
- **Encoding Search Queries**:
  - Utilises the **all-mpnet-base-v2 model** from **SentenceTransformers** to transform search queries into vector representations.
- **k-NN Search**:
  - Performs a **k-nearest neighbours** search on the `DescriptionVector` field in **Elasticsearch** to find the most relevant products.
- **Result Display**:
  - Retrieves and presents the **top matching products** based on similarity scores.

---

### **Streamlit Web Interface**
The frontend provides an intuitive web interface, featuring:
- **User Input**:
  - Users can enter a **search query** in a text input field.
- **Search Button**:
  - Triggers the semantic search when clicked.
- **Results Display**:
  - Presents product details (**name, description**) in a **user-friendly format**.

---
