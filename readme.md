
# Visionary Mate

Visionary Mate is a comprehensive web application that combines the functionalities of two projects—Multimodal Mate and Visionary—into a single platform. It provides multimodal assistance through text, images, audio, and documents, leveraging advanced AI models and APIs for real-time, context-aware responses.

## Features

- **Multimodal Input Processing**: Handles text, images, audio, and video inputs using the Gemini 1.5 Flash model.
- **Document-Based Queries**: Supports PDFs, PowerPoint, Excel, CSV, and JSON files with a Retrieval-Augmented Generation (RAG) pipeline.
- **Real-Time Assistance**: Provides voice and image processing for visually impaired users, with navigation and location services.
- **Real-Time Information Retrieval**: Integrates the Perplexity API for up-to-date information on current events and queries.

## Technologies Used

- **Frontend**: HTML, Tailwind CSS, JavaScript
- **Backend**: FastAPI
- **AI Models**: Gemini 1.5 Flash, HuggingFace Embeddings
- **APIs**: Google Cloud Text-to-Speech, Perplexity API

## Project Structure

```plaintext
visionary_mate/
├── main.py
├── .env
├── requirements.txt
├── credentials/
│   └── google_cloud_credentials.json
├── static/
│   └── app.js
├── templates/
│   ├── base.html
│   └── index.html
├── multimodal_mate/
│   ├── mate.py
│   ├── templates/
│   │   └── mate.html
│   └── static/
│       └── mate.js
└── visionary/
    ├── visionary.py
    ├── templates/
    │   └── visionary.html
    └── static/
        └── visionary.js
```

 RAG=>

**RAG (Retrieval-Augmented Generation)** is a technique used in natural language processing (NLP) and AI applications to enhance the performance of generative language models by integrating information retrieval capabilities. Developed initially by researchers at Facebook AI, RAG combines two core components:

1. **Retrieval**: Using a search or retrieval model, RAG identifies relevant documents or information from a large corpus of text (often stored in a vectorized, or embedding, format) based on a user query. This retrieval process provides context that may not be in the model’s immediate knowledge base.
2. **Generation**: A generative language model (like GPT or BERT) then uses this retrieved information to create a response, allowing it to answer questions more accurately and contextually.

### How RAG Works
1. **Retrieve Relevant Documents**: For a given query, RAG uses a retrieval mechanism to find relevant documents or chunks of text from a pre-indexed collection. This is often done with dense vector search techniques, such as using embeddings and similarity measures.
   
2. **Combine with the Model’s Response**: The generative model takes both the retrieved documents and the query as input to generate a response. The information retrieved guides the model, enabling it to be more precise and grounded in real-world data.

### Benefits of RAG

1. **Improved Accuracy**: By grounding responses in relevant documents, RAG improves the accuracy and factual correctness of language models, making it particularly useful in complex domains where up-to-date or specialized information is needed.

2. **Reduced Hallucination**: Language models sometimes "hallucinate" or generate plausible but incorrect information. RAG mitigates this by anchoring the response in real data, which helps prevent speculative or misleading answers.

3. **Scalability for Large Knowledge Bases**: RAG is effective in applications with extensive knowledge bases (like customer support or technical documentation), as it retrieves only the necessary information for each query, making the process more efficient.

4. **Versatile Use Cases**: RAG is highly adaptable and is beneficial for a variety of applications, such as answering knowledge-intensive questions, generating context-aware responses in chatbots, summarizing documents, and more.

In essence, RAG enhances a language model’s capabilities by allowing it to access and incorporate information beyond its inherent training, which is particularly advantageous in dynamic or specialized fields.

The flowchart above illustrates the Naive RAG pipeline used in Visionary Mate. The pipeline is divided into two sections: "Indexing" and "Augment".
Indexing

The "Indexing" section shows the process of indexing documents, which involves the following steps:
Tokenization
Stopword removal
Stemming
Lemmatization
Index creation
Augment

The "Augment" section shows the process of augmenting the indexed documents, which involves the following steps:
Prompt processing
Relevant document retrieval
Document ranking
Answer generation
Setup and Installation

Clone the Repository:
Bash
git clone https://github.com/yourusername/visionary_mate.git
cd visionary_mate
Install Dependencies:
Bash
pip install -r requirements.txt
Environment Variables:
Create a .env file in the root directory.
Add your API keys and other environment variables. Example .env content:
Env
GOOGLE_API_KEY=your_google_api_key_here
PERPLEXITY_API_KEY=your_perplexity_api_key_here
GOOGLE_APPLICATION_CREDENTIALS=credentials/google_cloud_credentials.json
Run the Application:
Bash
uvicorn main:app --reload
Access the Application:
Open your browser and go to http://127.0.0.1:8000.
Usage

Visionary: Provides real-time assistance for visually impaired users.
Multimodal Mate: Handles text, image, and document-based queries.
Troubleshooting

If you encounter issues with API keys, ensure that you have enabled the correct APIs in the Google Cloud Console.
If you encounter issues with dependencies, try updating requirements.txt and running pip install -r requirements.txt again.
Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.
Changelog

[Insert changes and updates here]
License

This project is licensed under the MIT License.
Contact

For any questions or feedback, please contact [your email].

Make sure to replace `flowchart.png` with the actual file name and path of the image you uploaded. Also, update the `yourusername` and `your email` placeholders with your actual GitHub username and email address.

