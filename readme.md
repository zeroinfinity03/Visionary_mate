
Here is the updated README.md file with the image and the flowchart description:

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

 RAG=>
<img src="https://github.com/user-attachments/assets/9f1365e4-31de-42b5-a16d-d4f79be8a2a3" alt="Screenshot" width="895">

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
```
