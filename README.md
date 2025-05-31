# HomeMatch: Real Estate AI Agent

## Overview

HomeMatch is an innovative application developed for "Future Homes Realty" that leverages large language models (LLMs) and vector databases to create personalized real estate listings. The application aims to enhance the property search experience by tailoring listings to individual buyer preferences.

This repository includes a Jupyter Notebook (`HomeMatch.ipynb`) that demonstrates the full workflow, from data generation to interactive search and personalized listing augmentation.

## Features

### 1. Understanding Buyer Preferences
- **Input Requirements**: Buyers can input their preferences, including:
  - Location
  - Property type
  - Budget
  - Amenities
  - Lifestyle choices
- **Natural Language Processing**: Utilizes LLMs to interpret buyer inputs, understanding nuanced requests beyond basic filters.
- **Interactive Quiz**: The notebook provides an interactive quiz where users answer a series of questions about their preferences. These answers are used to perform a semantic search and personalize property descriptions.

### 2. Integrating with a Vector Database
- **Property Storage**: Connects with a vector database (ChromaDB) to store all available property listings.
- **Vector Embeddings**: Matches properties with buyer preferences by focusing on:
  - Neighborhood vibes
  - Architectural styles
  - Proximity to specific amenities
- **Semantic Search**: Uses OpenAI embeddings and LangChain to perform similarity search between buyer preferences and property listings.

### 3. Personalized Listing Description Generation
- **Description Rewriting**: For each matched listing, the application uses an LLM to:
  - Rewrite descriptions to highlight aspects most relevant to the buyer’s preferences.
  - Ensure that personalization emphasizes appealing characteristics without altering factual information about the property.
- **Augmented Output**: The notebook demonstrates how the LLM augments listing descriptions based on the buyer's answers.

### 4. Listing Presentation
- **Output Format**: Outputs personalized listings as text descriptions, providing an engaging and tailored experience for potential buyers.
- **Notebook Output**: The notebook prints both the original and personalized descriptions for the top-matching listings.

## Notebook Workflow

The main steps in [`HomeMatch.ipynb`](HomeMatch.ipynb) are:
1. **Environment Setup**: Loads environment variables and required packages.
2. **Data Loading**: Loads synthetic real estate listings from `data/listings.json`.
3. **Vector Database Initialization**: Embeds and stores listings in a ChromaDB vector store.
4. **Semantic Search**: Performs similarity search using either hard-coded or interactive buyer preferences.
5. **Personalization**: Uses an LLM to rewrite listing descriptions to match buyer preferences.
6. **Interactive Quiz**: Allows users to input their preferences interactively and see personalized results.

## Getting Started

To set up the HomeMatch application, follow these steps:

1. Initialize a Python project and set up a virtual environment.
2. Install necessary packages: