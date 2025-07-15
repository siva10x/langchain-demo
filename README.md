# LangChain Demo

This project demonstrates how to use environment variables to securely manage secrets (like API keys) in Python, including usage in Jupyter notebooks.

## Project Structure

```
langchain-demo/
├── .env                        # Store secrets like API keys (not committed to git)
├── .gitignore                  # Ignore .env and other sensitive files
├── sample_openai_key.ipynb     # Jupyter notebook example
├── restaurant_name_generator.ipynb # Restaurant name generator notebook
└── ...                         # Other project files
```

## Setup Instructions
## Restaurant Name Generator Notebook

The `restaurant_name_generator.ipynb` notebook demonstrates how to use LangChain and OpenAI to generate creative restaurant names based on a given cuisine type.

### How it works
- Loads your OpenAI API key securely from the `.env` file using `python-dotenv`.
- Sets up a LangChain `ChatOpenAI` model with your API key.
- Prompts you to enter a cuisine type (e.g., Italian, Japanese, Mexican).
- Uses the model to generate and display a unique, catchy restaurant name for the specified cuisine.

### Usage
1. Ensure your `.env` file contains your OpenAI API key:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   ```
2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
3. Open `restaurant_name_generator.ipynb` in Jupyter and run the cells.
4. Enter a cuisine type when prompted to receive a suggested restaurant name.

### 1. Clone the Repository
```bash
git clone <your-repo-url>
cd langchain-demo
```

### 2. Create a Python Virtual Environment (Recommended)
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Required Packages
```bash
pip install -r requirements.txt
```

### 4. Add Your Secrets
Create a `.env` file in the project root:
```
OPENAI_API_KEY=your_openai_api_key_here
```

**Never commit your `.env` file to git!**

## Security Best Practices
- Always add `.env` to `.gitignore`.
- Never share or commit secrets to version control.

## Troubleshooting
- If you update `.env`, restart your Jupyter kernel to reload variables.

## License
MIT
