
# Medical Chatbot with RAG and FastAPI
# CareBot

This project is an AI-powered Medical Chatbot designed to provide medical information and assistance. It combines Retrieval-Augmented Generation (RAG) techniques, a pre-trained large language model (Phi-3-mini-128k-instruct), and a custom knowledge base to generate relevant and context-specific answers to user queries.

## Features:
- **Retrieval-Augmented Generation (RAG)**: Integrates a knowledge base for more accurate and contextually relevant answers.
- **FastAPI Backend**: A fast and efficient API to process user queries and deliver responses.
- **Customizable Knowledge Base**: Create and manage a domain-specific knowledge base using LangChain.
- **AI Model Integration**: Utilizes `microsoft/Phi-3-mini-128k-instruct` for text generation.
- **Interactive Query Handling**: Users can submit medical-related questions and receive precise answers.
- **Histogram Analysis**: Visualizes document token lengths for optimized chunking.

---

## 🛠️ Tech Stack

- **LLM**: Microsoft’s [`phi-3-mini-128k-instruct`](https://huggingface.co/microsoft/phi-3-mini-128k-instruct)  
- **RAG Framework**: LangChain for vector search & prompt formatting  
- **API**: FastAPI (Python)  
- **Frontend**: React.js  
- **Embedding**: HuggingFace or OpenAI embeddings  
- **Vector Store**: FAISS / ChromaDB (pluggable)

---


## How It Works:

### 1. **Knowledge Base Creation**:
- Text data is preprocessed using LangChain's Document and split into chunks for efficient retrieval using the `RecursiveCharacterTextSplitter`.

### 2. **Query Handling**:
- A user query is matched with relevant chunks from the knowledge base using vector similarity search (e.g., `KNOWLEDGE_VECTOR_DATABASE.similarity_search`).

### 3. **Prompt Construction**:
- The retrieved context and user query are formatted into a prompt using a pre-defined RAG template.

### 4. **Answer Generation**:
- The formatted prompt is passed to the Phi-3 model to generate a concise and contextually relevant answer.

### 5. **API Integration**:
- The FastAPI backend processes incoming user queries, retrieves context, formats the RAG prompt, and returns the AI-generated response.

## 💻 Local Setup

### 🔧 Backend (FastAPI)



This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
>>>>>>> cccde44 (Initial commit for Medical Chatbot project)
