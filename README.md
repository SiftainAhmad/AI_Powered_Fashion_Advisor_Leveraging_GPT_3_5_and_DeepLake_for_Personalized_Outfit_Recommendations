# AI_Powered_Fashion_Advisor_Leveraging_GPT_3_5_and_DeepLake_for_Personalized_Outfit_Recommendations

This notebook contains code for creating an outfit recommendation system using natural language processing and machine learning techniques. Here's a detailed summary of what the code is doing:
1. Data Import and Preprocessing:
   - Imports necessary libraries (numpy, pandas, matplotlib, seaborn).
   - Loads a CSV file containing luxury apparel product data.
   - Performs basic data cleaning by dropping null values and checking for duplicates.
   - Visualizes data distributions using various plots.
2. Text Preprocessing:
   - Defines a function to preprocess text data, including lowercasing, expanding contractions, and removing special characters.
   - Applies this preprocessing to the 'Description' column of the dataset.
3. Data Preparation for Machine Learning:
   - Converts the DataFrame to a dictionary format.
   - Creates Document objects for each product, containing the description as content and other details as metadata.
4. Text Splitting:
   - Uses CharacterTextSplitter to split long text descriptions into smaller chunks for better processing.
5. Embedding and Vector Store Creation:
   - Utilizes OpenAI's text-embedding-ada-002 model to create embeddings for the text chunks.
   - Creates a DeepLake vector store to store these embeddings and associated metadata.
6. Prompt Engineering:
   - Defines a template for generating outfit recommendations based on user input.
7. Recommendation Function:
   - Implements a function `display_top_similar_products` that:
     - Takes a user query and temperature parameter as input.
     - Searches the vector store for similar products.
     - Uses OpenAI's GPT-3.5-turbo-instruct model to generate recommendations.
     - Parses the model's output into a pandas DataFrame.
     - Displays the top 5 recommendations in an HTML table format, including links to Google image search for each product.
8. User Interface:
   - Provides an interactive interface where users can input their outfit requirements and desired creativity level (temperature).
   - Displays the recommendations based on the user's input.
     
Overall, this code creates a sophisticated outfit recommendation system that leverages natural language processing, embeddings, and large language models to provide personalized outfit suggestions based on user descriptions of occasions or events. It combines data preprocessing, machine learning techniques, and a user-friendly interface to deliver relevant and creative outfit recommendations.
