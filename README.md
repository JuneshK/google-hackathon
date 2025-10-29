
  <br />
      <img src="ai-policy-helper.png">
    </a>
  <br />

  <div align="center">
    <img src="https://img.shields.io/badge/-TypeScript-black?style=for-the-badge&logoColor=white&logo=typescript&color=3178C6"/>
    <img src="https://img.shields.io/badge/-Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" />
    <img src="https://img.shields.io/badge/Next.js-000?style=for-the-badge&logo=next.js&logoColor=white">

  </div>

<p align="center">
 
</p>

<h3 align="center">Auto Reply Email Chrome Extension</h3>
<p align="center"> BUILT-AI API GOOGLE HACKATHON 2025 
    <br> 
</p>

---

## 📝 Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Quick Start](#quickstart)
- [Deployment](#deployment)
- [Tech Stack](#techstack)
- [Contributing](../CONTRIBUTING.md)
- [Authors](#authors)
- [Acknowledgments](#acknowledgement)
- [Reference](#reference)

## 🧐 Introduction <a name = "introduction"></a>
For this project I intend to built a chrome extensions which will have a feature of replying emails . This extensions is focus to solve a issue for everyone who keep repeating same answers in reply . Hence , i design this extension so that every users can literally auto reply every email and don't need to manually type everything or open a new tab to use Gemini , ChatGPT and such .

## 🏁 Features <a name = "features"></a>




##  🚀 Software Architecture <a name = "System Design"></a>


- [Google Docs](https://docs.google.com/document/d/1sV751AAwvuBRCIP2oqekhdZM8vMNKaZtpbGtiVaYmTI/edit?usp=sharing) - View file to see the System Design


## <a name="quick-start">🤸 Quick Start</a>

**Prerequisites**

Make sure you have the following installed on your machine:

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en)
- [npm](https://www.npmjs.com/) (Node Package Manager)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) (Docker Desktop)



**Cloning the Repository**

```bash
git clone https://github.com/JuneshK/google-hackathon.git
cd google-hackathon
```



**Set Up Environment Variables**

Create a new file named `.env` in the root of your project and add the following content:

```env
# Backend
EMBEDDING_MODEL=local-384
LLM_PROVIDER=stub           # options: stub | openai | ollama
OPENAI_API_KEY=        # if using OpenAI, set this
OLLAMA_HOST=http://ollama:11434
VECTOR_STORE=qdrant         # qdrant | memory
COLLECTION_NAME=policy_helper
CHUNK_SIZE=700
CHUNK_OVERLAP=80

# Frontend
NEXT_PUBLIC_API_BASE=http://localhost:8000
```

Replace the placeholder values with your credentials. You can get these by signing up at: [**OpenAI API**](https://openai.com/index/openai-api/).




**Running the Project ( Method One)**

```bash
docker-compose up --build
```

Open [http://localhost:3000](http://localhost:3000) in your browser to view the Frontend <br>
Open [http://localhost:8000/docs](http://localhost:8000/docs) in your browser to view the Backend <br>
Open [http://localhost:6333](http://localhost:6333) in your browser to view the Database <br>
<br>
<small>⚠️ Note: The provided <code>docker-compose</code> setup fails due to issues with the Docker backend and connecting to the Qdrant database. As an alternative, I have implemented a <strong>manual run method</strong> for the project, which successfully starts all services and allows full functionality.</small>


<br>


## 📁 Project Structure

```
ai-policy-helper/
├─ backend/
│  ├─ app/
│  │  ├─ main.py          # FastAPI app + endpoints
│  │  ├─ settings.py      # config/env
│  │  ├─ rag.py           # embeddings, vector store, retrieval, generation
│  │  ├─ models.py        # pydantic models
│  │  ├─ ingest.py        # doc loader & chunker
│  │  ├─ __init__.py
│  │  └─ tests/
│  │     ├─ conftest.py
│  │     └─ test_api.py
│  ├─ requirements.txt
│  └─ Dockerfile
├─ frontend/
│  ├─ app/
│  │  ├─ page.tsx         # chat UI
│  │  ├─ layout.tsx
│  │  └─ globals.css
│  ├─ components/
│  │  ├─ Chat.tsx
│  │  └─ AdminPanel.tsx
│  ├─ lib/api.ts
│  ├─ package.json
│  ├─ tsconfig.json
│  ├─ next.config.js
│  └─ Dockerfile
├─ data/                  # sample policy docs
├─ docker-compose.yml
├─ Makefile
└─ .env.example
```

## 🎈 Demo Video <a name="demo-video"></a>
- [Google Drive](https://drive.google.com/drive/folders/1aeYDGklDoO1dJrGWMSyuYtgyGSfx8PGa?usp=drive_link) - Link to watch the demo of this project


## ⛏️ Built Using <a name = "built_using"></a>
- [Next.js](https://reactnative.dev/) - Web Framework
- [TailwindCSS](https://tailwindcss.com/) - CSS Framework
- [Typescript](https://www.typescriptlang.org/docs/) - Frontend Language


## ✍️ Authors <a name = "authors"></a>
- Myself

## 🎉 Acknowledgements <a name = "acknowledgement"></a>

  
## 🎉 References<a name = "reference"></a>
- [TailwindCSS](https://tailwindcss.com/) - How to Import Tailwind on Next.js
- [HelloInterview](https://www.hellointerview.com/learn/system-design/in-a-hurry/delivery) - System Design
- [Google Docs](https://docs.google.com/document/d/1irwxfSW1CIhFNfF-QptE0EOPVLqTquxpRPxOPc1X68Q/edit?usp=sharing) - Debugging & Challenges
