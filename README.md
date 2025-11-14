# Ollama_Project
Grocery List Categorizer with Ollama# 🛒 LLM-Powered Grocery List Categorizer

## 🌟 Overview

This project features a simple but practical Python script that leverages a **Large Language Model (LLM)**, accessed via **Ollama**, to automatically organize and categorize an unstructured grocery list.

By defining clear instructions in the prompt, the script transforms a messy text file into a clean, categorized, and alphabetized list, making your next shopping trip efficient and streamlined.

## 🚀 How It Works

The script is built around the `ollama` Python client and performs the following steps:

1.  **Configuration:** Sets the target LLM (defaulting to `llama3.2`) and defines the paths for input (`./data/grocery_list.txt`) and output (`./data/categorized_grocery_list.txt`) files.
2.  **Input Reading:** Checks for the existence of the input file and reads all grocery items from it.
3.  **Prompt Engineering:** Constructs a detailed prompt that instructs the LLM to:
    * Categorize items into common groups (e.g., Produce, Dairy, Bakery).
    * Sort items alphabetically *within* each category.
    * Present the results in a clear, organized bulleted format.
4.  **LLM Generation:** Sends the prompt and raw data to the running Ollama server using `ollama.generate()`.
5.  **Output Saving:** Prints the categorized list to the console and saves the final result to the designated output file.

## 🛠️ Prerequisites

To run this script, you must have the following installed and set up:

1.  **Ollama:** Installed and running on your local machine.
2.  **A Model:** The desired LLM model (e.g., `llama3.2`) must be downloaded via Ollama.
    ```bash
    ollama run llama3.2
    ```
3.  **Python 3.x:** Installed on your system.
4.  **Ollama Python Library:** Installed via pip.
    ```bash
    pip install ollama
    ```

## 📖 Usage

### 1. Set Up Files

First, create the necessary directory and the input file:

```bash
mkdir -p data
touch data/grocery_list.txt