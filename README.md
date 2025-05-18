# 🤖 Chat com PDFs Usando Azure AI Foundry

## 🌐 Visão Geral do Desafio

Neste projeto, usamos **Azure AI Foundry** para construir uma solução de chat interativo que responde com base no conteúdo de arquivos PDF. Essa arquitetura se apoia em **IA generativa**, **buscas vetoriais** e **embeddings**, permitindo criar um assistente virtual inteligente, fundamentado em documentos específicos, ideal para estudantes, pesquisadores e profissionais.

---

## 🎓 Cenário

Imagine-se como um estudante de Engenharia de Software desenvolvendo seu TCC. Com dezenas de artigos científicos em PDF acumulados, torna-se desafiador cruzar ideias, localizar trechos relevantes e gerar insights consistentes. Com o **Azure AI Foundry**, podemos montar um sistema que automatiza esse trabalho com tecnologia de ponta em IA.

---

## 🎯 Objetivos

- ✅ Carregar arquivos PDF com conteúdos acadêmicos.
- ✅ Criar embeddings vetoriais e indexar os documentos.
- ✅ Gerar respostas baseadas nas informações dos PDFs.
- ✅ Desenvolver um **chat interativo inteligente** para consultas contextuais.

---

## 🛠️ Tecnologias Utilizadas

- **Azure AI Foundry** – Plataforma modular para orquestração de soluções com IA.
- **Azure OpenAI Service** – Geração de texto via GPT-4 ou GPT-3.5.
- **Azure Cognitive Search** – Armazenamento e recuperação vetorial.
- **LangChain** – Pipeline de RAG (retrieval-augmented generation).
- **PyPDF2 / PyMuPDF** – Extração de texto dos PDFs.
- **Streamlit ou Gradio** – Interface do chat.

---

## 🔁 Fluxo da Solução com Azure AI Foundry

### 1. 📥 Ingestão de Dados
- Upload dos PDFs na camada de entrada do Foundry.
- Pré-processamento: extração de texto, segmentação em chunks.

### 2. 🧠 Geração de Embeddings
- Utilização do modelo `text-embedding-ada-002` via Azure OpenAI.
- Armazenamento dos vetores em **Azure Cognitive Search** com capacidade semântica.

### 3. 🔍 Recuperação + Geração (RAG)
- Consulta do usuário é convertida em embedding.
- Os vetores mais similares são recuperados e passados como contexto para o GPT.

### 4. 💬 Interface Interativa
- Usuário conversa com o chat.
- O sistema responde com base nos conteúdos encontrados nos documentos.

---

## ⚙️ Como Implementar com Azure AI Foundry

1. **Provisionar recursos no Azure:**
   - Azure AI Foundry
   - Azure OpenAI
   - Azure Cognitive Search
   - Azure Blob Storage (para os PDFs)

2. **Configurar pipelines no Foundry:**
   - Ingestão dos PDFs
   - Processamento e geração de embeddings
   - Integração com GPT para respostas geradas

3. **Deploy do front-end:**
   - Criar app com Streamlit/Gradio integrado via API do Foundry

---

## 📦 Estrutura Sugerida

```
📁 projeto-chat-foundry/
├── ingestao/
│   └── processar_pdfs.py
├── app/
│   └── chat_app.py
├── config/
│   └── foundry_pipeline.yaml
├── inputs/
│   └── documentos/
└── README.md
```

---

## 🚀 Benefícios da Solução com Azure AI Foundry

- Plataforma escalável, segura e modular.
- Fácil integração entre serviços de IA, dados e aplicações.
- Rápida prototipação e deploy de soluções de IA generativa.

---

## 📘 Referências

- [Azure AI Foundry Documentation](https://learn.microsoft.com/en-us/azure/ai-services/foundry/)
- [LangChain for RAG](https://docs.langchain.com/)
- [Azure OpenAI Service](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/)
- [Azure Cognitive Search](https://learn.microsoft.com/en-us/azure/search/)
