# MedBot: Medical Research Tool 

MedBot is a user-friendly medical research tool designed for effortless information retrieval. Users can input website URLs and ask questions to receive relevant insights from those websites.

![](medbot.jpg)

## Features

- Fetch website content by loading URLs or uploading text files with URLs.
- Use LangChain's UnstructuredURL Loader to process article content.
- Construct an embedding vector using OpenAI's embeddings and leverage FAISS, a powerful similarity search library, to enable swift and effective retrieval of relevant information
- Interact with the LLM's (Chatgpt) by inputting queries and receiving answers along with source URLs.


## Installation

1.Clone this repository to your local machine using:

```bash
  git clone https://github.com/kbthakur16/medical_research_tool.git
```
2. Install the required dependencies using pip:

```bash
  pip install -r requirements.txt
```
3.Set up your OpenAI API key in main.py file in the project.

```bash
  os.environ['OPENAI_API_KEY'] = 'Enter your openapi key here'
```
## Usage/Examples

1. Run the Streamlit app by executing:
```bash
streamlit run main.py

```

2.The web app will open in the browser.

- On the sidebar, we input URLs directly.

- Initiate the data loading and processing by clicking "Process URLs."

- Observe the system as it performs text splitting, generates embedding vectors, and efficiently indexes them using FAISS.

- The embeddings will be stored and indexed using FAISS, enhancing retrieval speed.

- The FAISS index will be saved in a local file path in pickle format for future use.
- One can now ask a question and get the answer based on those medical website
- I have used the following medical website
  - https://www.raysafe.com/products/x-ray-test-equipment
  - https://www.excedr.com/blog/medical-lab-equipment-list

## Project Structure

- main.py: The main Streamlit application script.
- requirements.txt: A list of required Python packages for the project.
- faiss_store_openai.pkl: A pickle file to store the FAISS index.
