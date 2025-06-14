# AI News Agent - Trend Spotter

A Google ADK-based agent that finds and reports on the latest AI agent trends specifically relevant to developers. This agent generates comprehensive reports on trends, releases, and common questions in the AI agent development space.

## Features

- **Automated Trend Analysis**: Discovers current AI agent trends using Google Search
- **Date-Aware Searches**: Uses date operators to find the most recent information (last 7 days)
- **Structured Reporting**: Generates reports with three key sections:
  - Top 5 Trends for Agent Developers
  - Top 5 Releases for Agent Developers
  - Top 5 Questions from Agent Developers
- **Developer-Focused**: Filters information specifically for relevance to developers building AI agents
- **Source Verification**: Includes verifiable source links for all reported information

## Setup

### Prerequisites

- Python 3.7+
- Google ADK

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/sjanagill/ai_news_agent.git
   cd ai_news_agent
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   # On Windows
   venv\Scripts\activate
   # On macOS/Linux
   source venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Install the package in development mode:
   ```bash
   pip install -e .
   ```

## Usage

To run the Trend Spotter agent:

```bash
# Using the ADK CLI
adk run trend_spotter
```

The agent will:
1. Determine the current date
2. Formulate search queries for the last 7 days
3. Execute searches to gather information
4. Analyze the results
5. Generate a structured report with trends, releases, and questions

## Project Structure

```
ai_news_agent/
├── trend_spotter/
│   ├── __init__.py
│   ├── agent.py      # Agent definition and configuration
│   └── prompt.py     # Detailed prompt instructions for the agent
├── pyproject.toml    # Project metadata and ADK configuration
└── requirements.txt  # Project dependencies
```

## How It Works

The agent uses the Gemini 2.0 Flash model with a detailed prompt that guides it through a multi-step process:

1. **Discovery**: Finds the current date
2. **Search**: Formulates and executes date-bounded search queries
3. **Analysis**: Filters information for developer relevance
4. **Reporting**: Creates a structured report with sourced information

## License

See the [LICENSE](LICENSE) file for details.