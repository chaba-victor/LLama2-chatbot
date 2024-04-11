

# Llama2 Medical Bot

The Llama2 Medical Bot is a powerful tool designed to provide medical information by answering user queries using state-of-the-art language models and vector stores. This README will guide you through the setup and usage of the Llama2 Medical Bot.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Important](#important)
- [License](#license)

## Prerequisites

Have these installed on your system first:

- Python 3.6 or higher
- Necessary Python packages (using pip or conda, whichever suits your prefference):
    - langchain
    - chainlit
    - sentence-transformers
    - faiss
    - PyPDF2 (for loading PDF document)

## Installation

1. Clone this repository to your local machine.

    ```bash
    git clone https://github.com/chaba-victor/Llama2-med-chatbot.git
    cd Llama2-med-chatbot
    ```

2. Create a Python virtual environment (venv or conda):

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use: venv\Scripts\activate

    conda create --name myenv python= # version 3.6 or higher
    conda activate # to activate your conda environment
    ```

3. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

4. Download the required language models`llama-2-7b-chat.ggmlv3.q8_0` and data. Please refer to the Langchain documentation for specific instructions on how to download and set up the language model and vector store.

5. Set up the necessary paths and configurations in your project, including the `DB_FAISS_PATH` variable and other configurations as per your needs.

## Recap

1. Set up your environment and install the required packages as described in the Installation section.

2. Configure your project by updating the `DB_FAISS_PATH` variable and any other custom configurations in the code.

3. Prepare the language model and data as per the Langchain documentation.

4. Start the bot by running the provided Python script (`python injest.py` and `chainlit run model.py`)or integrating it into your application.

## Usage

The Llama2 Medical Bot can be used for answering questions, in this case, medical-related queries. To use the bot, you can follow these steps:

1. Start the bot by running your application or using the provided Python script `langchain run model.py`.

2. Send a **medical-related** (since the data used is domain specific to medicine) query to the bot.

3. The bot will provide a response based on the information available in its database.

4. If sources are found, they will be provided alongside the answer.

5. The bot can be customized to return specific information based on the query and context provided.

## **Important*



1. Make sure to use only trusted docs as data to avoid prompt injection. You can also implement  input validation to check for malicious prompts before they are processed by the LLM.

2. If your aim is to interact with a model on specific fields, like in medicine for example, I suggest domain specific models like the quantized version of `mistral-7B` . Domain specific models are memory efficient, and more accurate (they are not prone to hallucinations)


Contributions to the Bot are welcome! 

## License

This project is licensed under the MIT License.

---

