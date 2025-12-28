# Agentic Design Patterns

This repository contains notebooks from [**Agentic Design Patterns: A Hands-On Guide to Building Intelligent Systems**](https://www.amazon.com/Agentic-Design-Patterns-Hands-Intelligent/dp/3032014018) by Antonio Gulli.

The code examples have been adapted and optimized for local development using Jupyter Lab with uv for dependency management.
Additionally, this repo only has examples that use LangChain/LangGraph, I will be adding the examples using google ADK in the future.

Original code can be found in this repo https://drive.google.com/drive/u/0/folders/1Y3U3IrYCiJ3E45Z8okR5eCg7OPnWQtPV

## Prerequisites

- **Python 3.11 or 3.12 or 3.13** (required)
- **uv** - Fast Python package installer and resolver

## Installation

### 1. Install uv

If you don't have uv installed:

```bash
# macOS/Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"

# Or via Homebrew (macOS)
brew install uv
```

### 2. Install Python 3.11+ (if needed)

Check your Python version:
```bash
python3 --version
```

If you need Python 3.11+:
```bash
# macOS (via Homebrew)
brew install python@3.11

# Or use uv's built-in Python management
uv python install 3.11
```

### 3. Clone and Setup

```bash
# Clone the repository
git clone <repository-url>
cd agentic_design_patterns

# Install dependencies and start Jupyter Lab
uv run jupyter lab
```

This will automatically:
- Create a virtual environment (`.venv/`)
- Install all required dependencies
- Launch Jupyter Lab in your browser

### 4. Configure API Keys

Create a `.env` file in the project root with your API keys:

```bash
# OpenAI (for chapter 1)
OPENAI_API_KEY=your_openai_api_key_here

```

## Project Structure

```
agentic_design_patterns/
├── chapter_1/           # Prompt Chaining examples
├── chapter_2/           # Routing patterns
├── pyproject.toml       # Project dependencies
├── .python-version      # Python version (3.11)
└── README.md
```

## Dependencies

This project uses the following key dependencies:
- `langchain` - Framework for building LLM applications
- `langchain-openai` - OpenAI integration
- `langchain-google-genai` - Google Gemini integration
- `langchain-anthropic` - Anthropic Claude integration
- `langgraph` - Graph-based agent workflows
- `jupyterlab` - Interactive notebook environment

All dependencies are managed via uv and specified in `pyproject.toml`.

## Usage

### Option 1: Running with Jupyter Lab (Browser-based)

Start Jupyter Lab in your browser:
```bash
uv run jupyter lab
```

This opens an interactive environment where you can run and edit notebooks.

### Option 2: Running with PyCharm (IDE-based)

**Requirements**: PyCharm Professional (Community Edition doesn't support Jupyter notebooks)

#### Initial Setup

1. **Open Project in PyCharm**
   ```bash
   # From terminal
   open -a "PyCharm" .

   # Or: File → Open → Select the agentic_design_patterns folder
   ```

2. **Configure Python Interpreter**
   - Bottom-right corner of PyCharm → Click on Python version
   - Select **Add New Interpreter** → **Add Local Interpreter**
   - Choose **Existing environment**
   - Click folder icon and navigate to:
     ```
     .venv/bin/python
     ```
   - Click **OK**

3. **Verify Interpreter**
   - Open any `.ipynb` file (e.g., `chapter_1/Prompt_Chaining.ipynb`)
   - PyCharm should recognize it as a Jupyter notebook
   - If prompted, click **Configure Jupyter Server** → **Managed Server**

#### Running Notebooks in PyCharm

- **Run a cell**: Click ▶️ play button or press `Shift+Enter`
- **Run all cells**: Right-click → **Run All Cells**
- **Add new cell**: Click `+` button or use keyboard shortcuts
- **View variables**: Check the **Variables** tab at the bottom
- **Interactive outputs**: Charts and visualizations render inline


### Common Commands

#### Adding New Dependencies
```bash
uv add package-name
```

#### Running Python Scripts
```bash
uv run python script.py
```

#### Updating Dependencies
```bash
uv sync
```