# GitLab's Chatbot

GitLab's Chatbot is a Retrieval-Augmented Generation (RAG) chatbot that interacts with document data (PDF, Markdown, HTML, and images with text). It uses a combination of vector search and a language model to answer user queries based on provided documents. This project is built with LangChain, OpenAI, and Panel for the user interface.

## Features

- **Multi-format Document Processing**: Supports PDFs, Markdown, HTML, and OCR for images.
- **Retrieval-Augmented Generation**: Combines document retrieval with language model generation for context-based answers.
- **Conversational Memory**: Remembers past interactions within the same session to provide contextually relevant responses.
- **User Feedback**: Allows users to rate responses and give feedback, aiding in performance evaluation and improvement.

## Requirements

To install the required packages, run:

```bash
pip install -r requirements.txt

## Dependencies
The following libraries are required:

openai: For embedding and language model API calls.
panel and param: To build the user interface.
langchain: To handle conversational chains, memory, and retrieval.
dotenv: To manage environment variables securely.
chroma-client: For vector storage and similarity search.
pdfplumber and tesseract: For handling PDF and OCR text extraction.
faiss-cpu: Optional, for faster vector search (if using FAISS as the backend for Chroma).

## Setup
1. API Keys
GitLab's Chatbot requires an OpenAI API key for embedding generation and LLM responses. To set up:

Create a .env file in the project root directory.

Add your OpenAI API key in the .env file:
OPENAI_API_KEY=your_openai_api_key_here

2. Running the Chatbot Locally
Install the requirements:
pip install -r requirements.txt
Launch the chatbot by running the main script in your environment.

Open the Panel dashboard in your browser to access the chat interface.

## Usage
Upload Documents: Load PDF or other supported files in the "Configure" tab.
Ask Questions: Type questions in the conversation tab to receive responses based on document content.
View Sources: After each response, view the document source in the "Database" tab to see which parts of the document were referenced.
Feedback: Provide feedback on responses for continuous improvement.

## Performance Evaluation
Quantitative Metrics:
- Answer relevance based on similarity scoring.
- Response accuracy (precision and recall).
Deploying on GitHub
To deploy GitLab's Chatbot on your GitHub repository:

Initialize a Git repository:
- git init
Add your files and commit:
- git add .
- git commit -m "Initial commit for GitLab's Chatbot"

Create a repository on GitHub and follow the instructions to link your local repository:
git remote add origin https://github.com/your_username/your_repository_name.git
git push -u origin main

## Future Enhancements
Additional Document Formats: Support for more file types such as Word documents.
Improved GUI: Add more customization and user controls in the interface.
Advanced Feedback Analysis: Automate feedback analysis to improve chatbot responses.

## Acknowledgments
Special thanks to the LangChain and Panel communities for their amazing tools that helped bring this project to life.
