
# 🚀 Spring AI Ollama Integration Platform

A full-stack application that demonstrates seamless integration of locally hosted Large Language Models (LLMs) using Ollama, built with Spring Boot and Spring AI.

This project focuses on enabling privacy-first, offline-capable AI applications with a clean backend architecture and an interactive React-based frontend.

---

## 📖 Overview

As organizations increasingly prioritize data privacy and cost efficiency, locally hosted LLMs are becoming a viable alternative to cloud-based AI services.

This project showcases how to:

* Integrate local LLMs using Ollama
* Build a scalable backend using Spring AI
* Provide a responsive UI for prompt testing and response visualization

---

## ✨ Core Features

* Local LLM execution via Ollama
* Spring AI-based abstraction layer
* RESTful API for prompt handling
* React-based UI for real-time interaction
* Configurable model parameters
* Fully offline-capable architecture

---

# 🏗️ System Architecture

## 🔷 High-Level Architecture Diagram

```
+-----------------------+
|   React Frontend UI   |
| (Prompt Input Layer)  |
+----------+------------+
           |
           | HTTP Requests (REST API)
           ▼
+------------------------------+
|   Spring Boot Backend        |
|   (Spring AI Integration)    |
|------------------------------|
| - Controller Layer           |
| - Service Layer              |
| - Ollama Client Integration  |
+--------------+---------------+
               |
               | Internal API Call
               ▼
+------------------------------+
|     Ollama Runtime           |
| (Local LLM Execution Engine) |
|------------------------------|
| - Model (LLaMA / Mistral)    |
| - Prompt Processing          |
| - Response Generation        |
+--------------+---------------+
               |
               ▼
        Response Returned
```

---

## 🔍 Architecture Breakdown

### 1. Frontend Layer (React UI)

* Provides a user-friendly interface for:

  * Entering prompts
  * Viewing model responses

* Sends HTTP requests to backend APIs

* Displays responses in real-time

---
<p align="center"><b><img width="1024" height="1226" alt="61f4aa34-d86e-4b49-a02a-b0bb7c138c39" src="https://github.com/user-attachments/assets/a9b8c465-d177-4d41-895b-6da8177ef049" />
</b></p>


### 2. Backend Layer (Spring Boot + Spring AI)

This is the core orchestration layer of the system.

#### Responsibilities:

* Exposes REST endpoints (`/api/ollama`)
* Processes incoming prompts
* Uses Spring AI to communicate with Ollama
* Handles response formatting and delivery

#### Internal Components:

* **Controller Layer** → Handles HTTP requests
* **Service Layer** → Business logic & prompt handling
* **Ollama Client** → Connects to local runtime

---

### 3. AI Execution Layer (Ollama Runtime)

* Runs locally on the developer’s machine
* Hosts open-source LLMs like:

  * LLaMA
  * Mistral

#### Responsibilities:

* Accepts prompt input
* Processes using selected model
* Generates and returns response

---

## 🔁 Request Flow

1. User enters a prompt in the React UI
2. UI sends request to `/api/ollama`
3. Spring Boot backend receives the request
4. Spring AI forwards the prompt to Ollama
5. Ollama processes the prompt using the local model
6. Response is returned to backend
7. Backend sends response back to UI
8. UI displays the result

---

## 🧠 Technical Highlights

* Implemented **local LLM orchestration** using Spring AI
* Designed a **layered backend architecture**
* Integrated **Ollama runtime for offline AI execution**
* Built a **clean and responsive frontend interface**
* Ensured **data privacy (no external API calls)**

---

## ⚙️ Prerequisites

* Java 17+
* Maven 3.6+
* Node.js + npm
* Ollama installed locally

---

## 🔧 Backend Setup

### Configure Application

```properties
spring.application.name=SpringAIDemo1
spring.ai.ollama.chat.options.model=deepseek-r1:1.5b
```

### Build & Run

```bash
mvn clean package -DskipTests
java -jar target/*.jar
```

---

## 🎨 Frontend Setup

```bash
cd src/main/llm-comparison-ui
npm install
npm run dev
```

---

## 🔌 API Endpoint

| Endpoint      | Description                         |
| ------------- | ----------------------------------- |
| `/api/ollama` | Generate response using local model |

---

## 🛠️ Technology Stack

**Backend**

* Spring Boot
* Spring AI

**Frontend**

* React.js

**AI Runtime**

* Ollama

---

## 💡 Use Cases

* Privacy-first AI applications
* Offline AI deployment
* Local LLM experimentation
* Cost-efficient AI solutions

---

## 🔮 Future Enhancements

* Streaming responses
* Multi-model selection (within Ollama)
* Chat history & session memory
* Docker deployment
* Enhanced UI/UX

---

## ⭐ Support

If you find this project useful, consider giving it a ⭐ on GitHub.
