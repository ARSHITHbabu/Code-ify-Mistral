# Code-ify-Mistral

A **terminal-based AI coding assistant** that uses **LangChain** and **MistralAI** to generate and execute Python code from natural language prompts.

Designed to simplify coding tasks by converting user instructions into executable Python code, this tool lets you iterate rapidly with the help of powerful LLMs.

---

## Project Overview

**code-ify-mistral** allows users to:

- Generate Python code from natural language using Mistral LLM
- Optionally execute the generated code safely within the same environment
- Interact through a lightweight terminal interface

Key Features:
- AI-powered Python code generation
- Instant execution of generated code
- Built with LangChain + MistralAI
- Simple CLI-based user experience
- Modular and easily extendable

---

## Tech Stack

- **AI Frameworks:** LangChain
- **Language Model:** Mistral via LangChain integration
- **Execution Backend:** Python `exec()` runtime
- **Prompt Management:** LangChain PromptTemplate
- **Language:** Python 3.8+

---

## Prerequisites

Ensure you have the following installed:
- Python 3.8 or higher
- A valid API key for MistralAI
- Git CLI

---

## Installation & Setup

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd code-ify-mistral
```

### 2. Set Up Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install transformers langchain_mistralai
```

### 4. Configure Environment Variables

Add your Mistral API key in your environment (or create a `.env` file if you prefer):

```python
import os
os.environ["MISTRAL_API_KEY"] = "your_mistral_api_key_here"
```

---

## Run the Assistant

Start the program by running the script:

```bash
python your_script_name.py
```

You'll be prompted to enter a task description. Example:

```text
Enter a coding task (or type 'exit' to quit): Sort a list of numbers
```

---

## Example Interaction

```text
Enter a coding task (or type 'exit' to quit): Sort a list of numbers

🔹 Generated Code:
```

```python
def sort_list(numbers):
    return sorted(numbers)

numbers = [5, 3, 8, 1]
print(sort_list(numbers))
```

```text
Do you want to execute this code? (yes/no): yes

🔹 Execution Output: [1, 3, 5, 8]
```

---

## Code Structure Overview

### `your_script_name.py`
> Main driver file that:
- Accepts user prompts
- Generates Python code using LangChain + Mistral
- Optionally executes the result

### `prompt_template`
> Uses LangChain's PromptTemplate to structure LLM input.

### `exec()`
> Python’s native `exec()` is used to run the generated code securely within a controlled session.

---

## License

This project is licensed under the **MIT License**.

---
