# What is Retrieval-Augmented Generation (RAG)?

![Alt text](images\image.png)

## Generation

LLMs can provide answers. But the issue is the fact comes out of his knowlegde, no source explicit provided.

> LLM Challenges:
> 1. **No Source**
> 2. **Out of date**
.
```If I ask "What planet in solar system has more moons?", it will probably say "Jupiter, with 80-ish moons".```

As of today, Saturn is the planet with more moons in the solar system.

## Retrieval Augmented

Retrieval helps briging context to the LLM about the facts regarding the questions.

So with RAG, the prompt will be composed with Retrieved Augmented data that helps answering the questions.

So before the prompt is sent to LLM, RAG will retrieve in a given set of data the piece of information that better fits in the question context, and will add that to the prompt.

```In the moons example, it could have a NASA article with a list of moons per planet, and add that to the prompt.```

## Simulated RAG example by ChatGPT
---
### System Instructions:
You are a factual assistant. Answer the question using only the information provided in the "Retrieved Context" section. If the answer is not available there, say "I don't know based on the provided information."

### User Question:
What planet in the solar system has more moons?

### Retrieved Context:
According to NASA’s latest report from 2023, Saturn has overtaken Jupiter in the number of confirmed moons. As of June 2023, Saturn has 145 confirmed natural satellites, while Jupiter has 95. This update comes after recent observations and discoveries made by the International Astronomical Union (IAU) which officially cataloged dozens of new Saturnian moons.

### Source:
- NASA - [https://solarsystem.nasa.gov](https://solarsystem.nasa.gov)
- IAU Moon Count Database

### LLM Output:

---

## RAG by ChatGPT

### How RAG Works – Step-by-Step
1. Query Processing:
    A user provides an input (e.g., a question or prompt).

2. Retriever Component:
    Instead of relying solely on the model's internal memory, RAG uses a retriever module (e.g., based on dense embeddings like DPR or sparse like BM25) to fetch relevant documents from an external knowledge base (e.g., Wikipedia).

3. Generator Component:
    The retrieved documents are passed as context to a pretrained generative model (like BART or T5), which then generates the final response conditioned on both the query and the retrieved documents.

### ✅ Key Benefits of RAG
* **Up-to-date information**: Unlike static models trained on fixed datasets, RAG can pull in fresh data from external sources.

* **Scalability**: The knowledge base can be updated or swapped without retraining the model.

* **Reduced hallucination**: The reliance on actual documents can help improve factual accuracy.


### 🔍 Real-world Use Cases
* Open-domain Question Answering (e.g., "What is the capital of Kazakhstan?")
* Customer Support Bots with access to support documents or FAQs
* Research assistants pulling information from academic papers
* Enterprise chatbots retrieving internal documentation

### 🛠️ Popular Libraries/Frameworks
* Hugging Face Transformers: Offers implementations of RAG using BART + DPR
* Haystack by deepset: Modular pipeline for building RAG-based search and QA systems
* **LangChain** / LlamaIndex: Modern frameworks for combining LLMs with retrieval over custom datasets