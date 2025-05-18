# 🤖 Chat Interativo com PDFs Usando Azure e IA Generativa

## 🧩 Visão Geral do Desafio

Neste projeto, desenvolvemos uma solução baseada em **Inteligência Artificial Generativa** usando **Azure Machine Learning** e **Azure Cognitive Services** para responder perguntas a partir do conteúdo de arquivos PDF. Utilizando **embeddings**, **busca vetorial** e **modelos de linguagem**, criamos um chat interativo que compreende e gera respostas contextualizadas com base em documentos acadêmicos.

## 🎓 Cenário

Imagine que você é um estudante de Engenharia de Software, prestes a escrever seu **TCC**. Com uma coleção crescente de artigos científicos em PDF, torna-se desafiador conectar ideias e extrair insights relevantes. Para resolver isso, criamos um sistema de **busca inteligente com IA**, que permite realizar perguntas sobre os documentos e obter respostas embasadas.

## 🎯 Objetivos

- ✅ Carregar arquivos PDF contendo informações relevantes.
- ✅ Implementar um sistema de **busca vetorial** para indexação.
- ✅ Utilizar **IA generativa** para responder com base nos documentos.
- ✅ Desenvolver um **chat interativo** para consultas em linguagem natural.

## 🛠️ Tecnologias Utilizadas

- **Azure Machine Learning** – Orquestração e deploy de modelos.
- **Azure Cognitive Search** – Indexação e busca vetorial.
- **Azure OpenAI Service** – Geração de respostas com GPT.
- **Python (LangChain, PyPDF, FAISS)** – Pré-processamento e execução local.
- **Streamlit ou Flask** – Interface do chat.

## 🧪 Etapas da Solução

### 1. 💾 Carregamento de PDFs
- Extração do texto com `PyMuPDF` ou `PyPDF2`.
- Divisão em chunks com `LangChain` para melhor processamento.

### 2. 🔍 Geração e Armazenamento de Embeddings
- Uso de `Azure OpenAI Embeddings` (modelo `text-embedding-ada-002`).
- Armazenamento vetorial com **FAISS** ou **Azure Cognitive Search**.

### 3. 🧠 Consulta com IA Generativa
- O usuário envia uma pergunta.
- O sistema busca os vetores mais relevantes.
- O conteúdo é passado ao modelo GPT para gerar a resposta.

### 4. 💬 Interface Interativa
- Desenvolvimento de um front-end simples com Streamlit ou Flask.
- Campo de upload de PDFs e campo de chat.

## 🧭 Execução no Azure

### 🔹 Etapa 1: Provisionamento dos Serviços
- Criar instância do **Azure Machine Learning Workspace**.
- Criar recursos do **Azure OpenAI** e **Azure Cognitive Search**.

### 🔹 Etapa 2: Pipeline de Processamento
- Notebook de pré-processamento dos PDFs.
- Criação de embeddings e envio para o índice vetorial.

### 🔹 Etapa 3: Deploy do Chat
- Deploy do app com Streamlit via Azure App Service.
- Integração com API do Azure OpenAI para consultas em tempo real.

## 📦 Estrutura do Projeto

```
📁 projeto-chat-pdf/
├── notebooks/
│   └── processar_pdfs.ipynb
├── app/
│   └── app_chat.py
├── inputs/
│   └── artigos.pdf
├── requirements.txt
└── README.md
```


