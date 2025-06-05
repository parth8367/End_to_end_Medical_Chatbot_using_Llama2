# End-to-end-Medical-Chatbot-using-Llama2

This project demonstrates how to build a conversational chatbot using the [Llama_2](https://ai.meta.com/resources/models-and-libraries/llama-downloads/) model.  A PDF containing medical information is indexed with Pinecone and queried via a Flask web interface.

## Features

- **Document ingestion** – Medical_book.pdf is split into text chunks and embedded with `sentence-transformers`.
- **Pinecone vector store** – The embeddings are stored and searched using Pinecone.
- **Llama 2 inference** – Responses are generated locally with a quantized Llama 2 model via `ctransformers`.
- **Web chat UI** – A simple Bootstrap interface allows interactive Q&A with the bot.

## How to run?
### STEPS:

Clone the repository

```bash
Project repo: https://github.com/
```

### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n mchatbot python=3.8 -y
```

```bash
conda activate mchatbot
```

### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


### Create a `.env` file in the root directory and add your Pinecone credentials as follows:

```ini
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
PINECONE_API_ENV = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```


### Download the quantize model from the link provided in model folder & keep the model in the model directory:

```ini
## Download the Llama 2 Model:

llama-2-7b-chat.ggmlv3.q4_0.bin


## From the following link:
https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/tree/main
```

```bash
# run the following command
python store_index.py
```

```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up localhost:
```


### Techstack Used:

- Python
- LangChain
- Flask
- Meta Llama2
- Pinecone


