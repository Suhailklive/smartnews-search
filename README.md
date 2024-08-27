# SmartNewsSearch: News Research Tool

SmartNewsSearch is a user-friendly news research tool designed for effortless information retrieval. It allows users to input article URLs and ask questions to receive relevant insights from news articles, particularly in the stock market and financial domains.

![](newsResearchtool.jpg)

## Features

- **Load URLs or Upload Text Files:** Fetch article content by entering URLs directly or uploading text files containing URLs.
- **Process Content:** Use LangChain's UnstructuredURL Loader to extract article content.
- **Generate Embeddings:** Construct embedding vectors using OpenAI's embeddings.
- **Efficient Retrieval:** Leverage FAISS, a powerful similarity search library, for fast and effective retrieval of relevant information.
- **Interact with LLM:** Input queries to ChatGPT and receive answers along with source URLs.


## Usage/Examples

1. **Run the Streamlit App:**

    ```
    streamlit run main.py
    ```

2. **Interact with the Web App:**
    - The web app will open in your browser.
    - On the sidebar, you can input URLs directly or upload text files.
    - Click "Process URLs" to initiate data loading and processing.
    - The system will handle text splitting, generate embedding vectors, and index them using FAISS.
    - The FAISS index will be stored in a local file (`faiss_store_openai.pkl`) for future use.
    - Ask questions to retrieve answers based on the processed news articles.

3. **Example Articles Used:**
    - [Tata Motors Gains Certificates for Production-Linked Payouts](https://www.moneycontrol.com/news/business/tata-motors-mahindra-gain-certificates-for-production-linked-payouts-11281691.html)
    - [Tata Motors Launches Punch ICNG: Price Starts at Rs 7.1 Lakh](https://www.moneycontrol.com/news/business/tata-motors-launches-punch-icng-price-starts-at-rs-7-1-lakh-11098751.html)
    - [Buy Tata Motors: Target of Rs 743 - KR Choksey](https://www.moneycontrol.com/news/business/stocks/buy-tata-motors-target-of-rs-743-kr-choksey-11080811.html)

## Project Structure

- **`main.py`**: The main Streamlit application script.
- **`requirements.txt`**: A list of required Python packages for the project.
- **`faiss_store_openai.pkl`**: Pickle file storing the FAISS index.
- **`.env`**: Configuration file for storing your OpenAI API key.
