# AI QA over PDF & documents

A **minimal** code base for creating AI apps to do Question Answering (QA) over PDF documents, completely **locally**.

<img src="ai-starter-kit.png" />

This project is inspired by [local-ai-stack](https://github.com/ykhli/local-ai-stack). However, their stack is entirely javascript based, and I needed a python based _backend_, so decided to create this project.



https://github.com/undersky0827/QA-document-learning/assets/3600972/fba21d09-336e-4861-bfb6-abbc57aab635



## Stack

- 🦙 Inference: [Ollama](https://github.com/jmorganca/ollama)
- 💻 VectorDB: [Qdrant](https://github.com/qdrant/qdrant)
- 🧠 LLM Orchestration: [Langchain](https://python.langchain.com/docs/get_started/introduction)
- 🖼️ App logic: [FastAPI](https://fastapi.tiangolo.com/)

## How to get started

1. Clone this repo:

```bash
git@github.com:undersky0827/QA-document-learning.git
```

2. Install backend dependencies:

```bash
cd backend/app
pip install -r requirements.txt
```

3. Install frontend dependencies:

```bash
cd frontend
npm install
```

4. Start the Qdrant vector database (you need Docker). See [here](https://github.com/qdrant/qdrant) for other options information:

```bash
docker run -p 6333:6333 qdrant/qdrant
```

5. Install Ollama
   Instructions are [here](https://github.com/jmorganca/ollama#ollama)

6. Run the FastApi server (from inside `backend` directory):

```bash
python app/main.py
```

7. Open a new terminal and start the React development server (from inside `frontend`):

```bash
npm start
```

## Change Configurations

You can change configurations in `.config` file, such as the _embedding model_, _chunk size_, and _chunk overlap_. If you plan to use Qdrant Cloud, you can or you can create your own `.env` file and set necessary api keys.

## Additional Use Cases

Although current app only support pdf files, it's very straightforward to add other types of files such as text files, etc. Also, you can easily add the open-ended chat in addition to QA over document use case.

