# Learning LangGraph

This repository contains a series of Jupyter notebooks that I have created while learning **LangGraph**.

## Setup

### OpenAI API Key
To run the notebooks you need an OpenAI api key.

```bash
echo "OPENAI_API_KEY=your-api-key-here" > .env
```

### Setting up the Kernel
You also need to have Python installed along with the necessary dependencies. You can set up a virtual environment and install them with:

```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
pip install -r requirements.txt
```


After activating your virtual environment, install the Jupyter kernel package:

```bash
pip install ipykernel
```

Then, add the virtual environment as a kernel:

```bash
python -m ipykernel install --user --name=venv --display-name "AI-ENG-ENV"
```
Now, when you open Jupyter Notebook, you should see "AI-ENG-ENV" as an available kernel.


## Running the Notebooks
After installing the dependencies and setting up the kernel, launch Jupyter Notebook from the root directory:

```bash
jupyter notebook
```
Then, open any of the .ipynb files and select the Python (venv) kernel to ensure the correct environment is used.

## Notebooks

Each notebook explores different aspects of LangGraph, including:

- **Minimal chatbot** – The minimal chatbot that is able to remember previous messages.
- **Minimal React Agent** - A minimal Agent to do basic arithmetic, uses tools_condition.
- **🐾 Pet Info chatbot** - This project is an example of building a multi-turn conversational agent with structured state using LangGraph. It guides a user through a short conversation to determine:
  - whether they have a pet, 
  - what kind of animal it is, 
  - and the pet's name. 
  
  It demonstrates the following concepts:
  - Tool calling with LangChain + LangGraph: the agent uses an explicit pet_info tool call on every turn to capture known information. 
  - State management with multiple fields: the graph state tracks has_pet, animal, pet_name, and messages independently. 
  - Graph architecture with multiple nodes:
    - A node to get user input 
    - A node to let the agent process and call the tool 
    - A final node to summarize and end the conversation 
  - Letting the agent drive the flow: the agent decides when the conversation is over based on known data (e.g. all fields filled or user has no pet). 
  - Streaming execution: the LangGraph is run in streaming mode to simulate a real-time chatbot loop. 
  - Clean return structure: after the conversation ends, the final dict contains the gathered information (or indicates the user has no pet).
  This is a useful starting point for building more complex assistant flows that combine structured tool use with natural conversation.


