# SeshatAIBE

Backend submodule for the SeshatAI fullstack application. Awaits client calls from the frontend, performs RAG retrieval against the mythology knowledge base, handles translation, and forwards context to the Grok AI service.

## Tech Stack

- **Runtime:** Node.js
- **Testing:** Jest
- **AI Integration:** Grok AI
- **Vector Store:** Qdrant
- **Embeddings:** Ollama
- **Code Quality:** SonarQube
- **Translation:** Translation API

## Getting Started

### Prerequisites
- Node.js >= 18
- npm >= 9
- A valid Grok API key
- A valid translation API key
- Qdrant running locally (`docker run -p 6333:6333 qdrant/qdrant`)
- Ollama installed with the embedding model pulled (`ollama pull nomic-embed-text`)

### Installation
```bash
npm install
```

### Development Server
```bash
npm run dev
```

### Build
```bash
npm run build
```

### Testing
```bash
npm test
```

### Linting
```bash
npm run lint
```

## Environment Variables

Create a `.env` file in the root directory:

```env
PORT=3000
GROQ_API_KEY=your_grok_api_key
TRANSLATION_API_KEY=your_translation_api_key
```

## Code Quality

This project uses SonarQube for static code analysis. Configuration is defined in `sonar-project.properties`.

To run an analysis locally:
```bash
sonar-scanner
```

## Related

- [SeshatAIFE](https://github.com/Adrian55Stack/SeshatAIFE) — Frontend submodule
- [SeshatAI](https://github.com/Adrian55Stack/SeshatAI) — Monorepo