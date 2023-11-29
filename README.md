# Product Search with LangChain and Llama2

## Overview
This project leverages Langchain framework, open-source Llama2 LLM, and retrieval-augmented generation (RAG) method to build a working product search engine on a single T4 GPU.

## Method
- **Model:** Meta's LLama2 from HuggingFace, with 4-bit quantization and LoRA 
- **Data:** [WDC Product Dataset](https://huggingface.co/datasets/wdc/products-2017)
- **Framework:** [Langchain](https://python.langchain.com/docs/get_started/introduction.html)
- **Embedding:** [Instruction fine-tuned text embedding](https://huggingface.co/hkunlp/instructor-large), [VectorDB](https://python.langchain.com/docs/integrations/vectorstores/chroma)

The whole process is demonstrated in the repo's jupyter notebook.

## Working App
The working app was built using Streamlit.

Upon launching, it takes about a minute for the app to load the dependencies.

Once all are succesfully loaded, this is the interface of the app:

<img src="screenshots/llm-search.png" alt="llm-search"/>

Type the query in the query box:

<img src="screenshots/llm-search-query.png" alt="llm-search-query"/>

The app will search and return an answer to the user question:

<img src="screenshots/llm-search-response.png" alt="llm-search-response"/>

For reference, the expander contains the retrieved products (with the metadata):

<img src="screenshots/llm-search-retrieved-docs.png" alt="llm-search-retrieved-docs"/>
