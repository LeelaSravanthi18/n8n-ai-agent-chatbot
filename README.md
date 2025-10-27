# n8n AI Agent Chatbot

This project contains an **n8n workflow** that builds a powerful **AI Chatbot Agent** using **OpenAI**, **LangChain**, and **SerpAPI**.  
It receives chat messages, processes them intelligently using GPT, remembers previous context, and can search the web for answers.

## Features

**Chat Trigger:**  
Listens for incoming chat messages via n8n’s Chat Trigger node.

**AI Agent Integration:**  
Powered by LangChain’s Agent node — handles logic, reasoning, and dynamic tool use.

**OpenAI Chat Model:**  
Uses the `gpt-4.1-mini` model for conversational AI.

**Memory Management:**  
Maintains recent chat history using a **Memory Buffer Window** node, enabling contextual conversation.

**Web Search (SerpAPI):**  
Integrates real-time web search results into the AI’s responses for up-to-date answers.

**Fully No-Code Setup:**  
Easily extendable in the [n8n.io](https://n8n.io) workflow editor.

## Workflow Overview

### 1. **When Chat Message Received**
- Node: `@n8n/n8n-nodes-langchain.chatTrigger`
- Public chat trigger that activates when a user sends a message.

### 2. **AI Agent**
- Node: `@n8n/n8n-nodes-langchain.agent`
- The brain of the workflow.
- Connects with language model, memory, and tools to generate responses.

### 3. **OpenAI Chat Model**
- Node: `@n8n/n8n-nodes-langchain.lmChatOpenAi`
- Model used: **gpt-4.1-mini**
- Credential: Your OpenAI API key (OAuth2)
- Generates smart and natural responses.

### 4. **Simple Memory**
- Node: `@n8n/n8n-nodes-langchain.memoryBufferWindow`
- Remembers recent messages for conversational context.

### 5. **SerpAPI Tool**
- Node: `@n8n/n8n-nodes-langchain.toolSerpApi`
- Provides access to real-time web data for answering current or factual queries.

## 🔗 Workflow Connections
<img width="1915" height="964" alt="image" src="https://github.com/user-attachments/assets/e5003889-a13e-4317-adb2-28914f03f7ea" />


