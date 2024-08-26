# Website Assistant

A full-stack application utilizing OpenAI, Flask, React, and Pinecone to provide interactive insights from web pages.

This project demonstrates how to build a comprehensive application that allows users to input a URL and query
information about the content of that webpage. It showcases the integration of Retrieval Augmented Generation (RAG),
OpenAI's APIs, and vector databases.

## Overview

**Website Assistant** is a sample application. It consists of the following main components:

- **Backend (Flask)**: Manages website scraping, uses OpenAI's Embeddings API to create text embeddings, and stores
  these embeddings in the Pinecone vector database. It also retrieves relevant text to assist the LLM in answering user
  queries.

- **OpenAI**: Utilizes two APIs:
    - **Embeddings API**: Embeds the text of the website and user questions.
    - **ChatCompletions API**: Provides answers from GPT-4 based on the generated embeddings.

- **Pinecone**: Serves as the vector database for:
    - Storing embeddings of the website's text.
    - Retrieving the most relevant text chunks to construct prompts for the LLM.

- **Frontend (React)**: Offers the user interface for inputting URLs and asking questions about the webpage content.

## Setup

Follow these steps to set up and run the application locally:

1. **Install Python Dependencies**

   Navigate to the root directory of the project and install the required Python packages:

   ```bash
   pip install -r requirements.txt

2. **Install React Dependencies**

   Change to the client directory and install the necessary React packages:

   ```bash
    cd client
    npm install

3. **Configure Environment Variables**

   Create a .env file in the root directory and add the following environment variables:

   ```env
    OPENAI_API_KEY=<YOUR_OPENAI_API_KEY>
    PINECONE_API_KEY=<YOUR_PINECONE_API_KEY>
    ```

   Replace `<YOUR_OPENAI_API_KEY>` and `<YOUR_PINECONE_API_KEY>` with your actual API keys.

4. **Start the Flask Server**

   From the root directory, start the Flask server:

    ```bash
    python run.py

5. **Start the React App**

   In a new terminal window, navigate to the client directory and start the React application:

    ```bash
    cd client
    npm start
   ```

   The React app should now be running on http://localhost:3000.

## Usage

1. Open your browser and navigate to http://localhost:3000.
2. Enter a URL of the webpage you want to analyze.
3. Ask questions about the content of the webpage.

The application will process the input and provide responses based on the content of the specified webpage.

## Contributing

Contributions to this project are welcome! If you have suggestions or improvements, please open an issue or submit a
pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments

- OpenAI for providing powerful language models and APIs.
- Pinecone for offering a robust vector database solution.
- React for building the user interface.
- Flask for creating the backend service.
