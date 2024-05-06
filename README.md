<div align="center">
  <h1>PDF Summarizer</h1>
</div>

Overview
-----------------
This project automates the summarization of PDF documents using a Large Language Model (LLM) chain. The application reads a PDF document, processes its content with a chain of models, and outputs a concise summary.

Installation
-----------------------
Prerequisites
Ensure you have Python installed on your machine. Python 3.8 or newer is recommended.

Dependencies
---------------------
Install the necessary Python libraries by running the following command in your terminal:


pip install langchain-community 
pip install langchain-core 
pip install langchain-openai
pip install pypdf2


To run the project, follow these steps:
----------------------------------------

Place your target PDF documents in the PDF directory within your project folder.
Open your terminal and navigate to the project directory.
Run the script using the following command:

python name_of_your_script.py

Replace name_of_your_script.py with the actual name of your Python script.

Code Structure
-------------------
Document Loading: The PyPDFLoader class from the langchain_community.document_loaders.pdf module is used to load PDF documents.
Prompt Template: A custom prompt template is created to instruct the language model on how to process the document.
Language Model Configuration: The ChatOpenAI class is configured with necessary parameters (from config.py) to interact with OpenAI's language models.
Model Chain Setup: The LLMChain class integrates the language model with the prompt, while StuffDocumentsChain handles the interaction flow and execution based on the document content.
Configurations
Configure the language model parameters in the config.py file. This includes API keys and settings related to the OpenAI model used.

Custom Models
This project uses custom classes (Custom_LLMChain, StuffDocumentsChain) for handling specific logic and interactions. These classes encapsulate the details necessary for integrating different components and managing the data flow.
