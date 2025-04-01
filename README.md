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


