# LLM Text Summarization with Langchain & LM Studio

This project contains a Jupyter Notebook (`summarization_tool.ipynb`) designed to perform text summarization using a Large Language Model (LLM) hosted locally with [LM Studio](https://lmstudio.ai/). It utilizes the `langchain` framework to interact with the LLM and generate concise summaries from longer text inputs.

## Description

The notebook provides a straightforward example of how to:
* Connect to an LLM running in LM Studio using `langchain_openai.ChatOpenAI`.
* Define a prompt template for the summarization task.
* Input a sample text.
* Invoke the LLM to generate a summary of the text.
* Print the resulting summary.

This is a basic tool meant for users who want to quickly get started with text summarization using their own local LLM setup.

## Features

* **Local LLM Summarization:** Performs text summarization using an LLM running locally via LM Studio.
* **Langchain Integration:** Uses the `langchain` library for LLM interaction and prompt management.
* **Simple Interface:** Easy-to-use Jupyter Notebook format.
* **Customizable Model:** Users can specify the model served by LM Studio (though the notebook defaults to "google/gemma-3-1b" as an example).
* **Example Text Provided:** Includes a sample text for quick testing.

## Getting Started

### Prerequisites

* **Python 3.x:** Ensure you have Python installed.
* **pip:** Python package installer.
* **Jupyter Notebook or JupyterLab:** To run the `.ipynb` file.
* **LM Studio:** Download and install LM Studio from [lmstudio.ai](https://lmstudio.ai/).
* **A Large Language Model:** Download a compatible LLM within LM Studio (e.g., Gemma, Llama, Mistral). Ensure the model is loaded and the local server is running in LM Studio.

### Installation

1.  **Clone the repository (or download the notebook):**
    ```bash
    # If it were a full repository:
    # git clone [https://github.com/Daniel-Rukes/Summary-LLM.git](https://github.com/Daniel-Rukes/Summary-LLM.git)
    # cd Summary-LLM

    # For now, just ensure you have the summarization_tool.ipynb file.
    ```

2.  **Install the required Python packages:**
    Open your terminal or command prompt and run:
    ```bash
    pip install langchain langchain_openai
    ```
    *(You might also need `jupyter` if you haven't installed it yet: `pip install notebook`)*

### Configuration

1.  **Start LM Studio:**
    * Open LM Studio.
    * Load the desired LLM (e.g., `google/gemma-3-1b` or any other model you have).
    * Navigate to the "Local Server" tab (usually represented by `<->`).
    * Start the server. By default, it should run on `http://localhost:1234/v1`.

2.  **Verify Notebook Configuration:**
    * Open `summarization_tool.ipynb`.
    * In the cell where `ChatOpenAI` is instantiated, ensure the `base_url` matches your LM Studio server address (default is `http://localhost:1234/v1`).
    * The `model` parameter in `ChatOpenAI` can often be a placeholder when using LM Studio, as LM Studio serves the model currently loaded in its UI. You can leave it or try specifying the exact model name you have loaded in LM Studio.

### Usage

1.  **Launch Jupyter Notebook or JupyterLab:**
    ```bash
    jupyter notebook
    # or
    jupyter lab
    ```
2.  Open the `summarization_tool.ipynb` notebook.
3.  **Modify Input Text (Optional):**
    * Locate the cell containing the `example_text` variable.
    * You can replace the sample text with any other text you wish to summarize.
4.  **Run the Cells:**
    * Execute the cells in the notebook sequentially from