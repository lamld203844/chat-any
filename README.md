# Chat-any (chat with any website)

## 1. Introduction

A Retrieval-Augmented Generation (RAG) system is a cutting-edge approach in natural language processing that combines retrieval-based and generation-based models to create highly accurate and contextually aware responses. In building such a system, leveraging the LlamaIndex framework facilitates efficient and dynamic interaction with vast amounts of web-based data. By employing the BAAI/bga-small-en model for embeddings, the system can generate high-quality vector representations of text, enhancing its ability to understand and retrieve relevant information from diverse web sources. The use of the Gemini-pro model as the large language model (LLM) ensures sophisticated and coherent generation of responses, enabling the RAG system to engage in meaningful and contextually appropriate dialogues. This amalgamation of advanced retrieval techniques and powerful generative capabilities allows for the development of a robust system capable of delivering precise and informative interactions with any website, making it a versatile tool for various applications, from customer support to research assistance.

## 2. Overview

- System architecture
    
    ![system-architecture.drawio.png](./asset/system-architecture.png)
    

The process begins by user inputing website URL. After that, a website is crawled and convert its content into text. This text is then split and embedded using the embeddings model. When a user inputs a prompt, the system performs a similarity search in the embedding space to find relevant information, which is then augmented to the original prompt. This augmented prompt is sent to the large language model (LLM), which generates a detailed and contextually appropriate response that is returned to the user. This system leverages advanced retrieval and generation techniques to provide accurate and relevant answers based on the content of the crawled website.

## 3. Installation

- First, clone this repository
    
    ```python
    cd repo-name
    ```
    
- Install dependencies
    
    ```python
    !pip install -r requirements.txt 
    ```
    
- Because, we use Gemini-pro as LLM, so you may need to get Gemini API Key. [Get an API key](https://makersuite.google.com/app/apikey). Once you have Google API key, add it into .env file
- **Optional**
    
    Because 
    

## 4. Usage

- To run demo app with Streamlit
    
    ```python
    streamlit run app.py
    ```
    

# Demo

9. demonstrate at least how-to-installation, and highlight all possible usages of your application.

## Limits

- Can only handle **english** language (Because I use [Huggingface: BAAI/bge-small-en](https://huggingface.co/BAAI/bge-small-en) as embedding model)