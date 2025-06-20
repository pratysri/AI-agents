# AI Agents Collection

A collection of AI-powered agents for web scraping, data extraction, and developer tool research. This repository contains two distinct agents built with modern AI frameworks.

## 🚀 Projects

### 1. Simple Agent (`simple-agent/`)
A basic web scraping agent that uses **Model Context Protocol (MCP)** with Firecrawl to scrape websites and extract data through natural language queries.

**Key Features:**
- Real-time web scraping using Firecrawl MCP server
- Natural language interface for data extraction
- Integration with OpenAI GPT-4o-mini for intelligent responses
- Interactive chat-based interface

**Technology Stack:**
- LangChain MCP Adapters
- LangGraph for agent orchestration
- OpenAI GPT-4o-mini
- Firecrawl for web scraping

### 2. Advanced Agent (`advanced-agent/`)
A sophisticated research agent that analyzes developer tools and technologies, providing structured comparisons and recommendations.

**Key Features:**
- Multi-step research workflow using LangGraph
- Structured analysis of developer tools and companies
- Automated extraction of pricing, tech stack, and API information
- Intelligent recommendations based on developer needs

**Technology Stack:**
- LangGraph for workflow orchestration
- Firecrawl for web scraping and search
- Pydantic for data validation
- OpenAI GPT-4o-mini for analysis

## 🛠️ Architecture

### Simple Agent Architecture
```
User Input → LangGraph Agent → MCP Tools → Firecrawl → Web Data → Structured Response
```

### Advanced Agent Architecture
```
Query → Extract Tools → Research Companies → Analyze Data → Generate Recommendations
```

## 📋 Prerequisites

- Python 3.12+
- OpenAI API Key
- Firecrawl API Key
- Node.js (for MCP server)

## 🔧 Setup

### 1. Clone the Repository
```bash
git clone <your-repo-url>
cd AI-agents
```

### 2. Environment Setup
Create `.env` files in both project directories:

**simple-agent/.env:**
```env
OPENAI_API_KEY=your_openai_api_key_here
FIRECRAWL_API_KEY=your_firecrawl_api_key_here
```

**advanced-agent/.env:**
```env
OPENAI_API_KEY=your_openai_api_key_here
FIRECRAWL_API_KEY=your_firecrawl_api_key_here
```

### 3. Install Dependencies

**For Simple Agent:**
```bash
cd simple-agent
uv sync
```

**For Advanced Agent:**
```bash
cd advanced-agent
uv sync
```

### 4. Install MCP Server (for Simple Agent)
```bash
npm install -g firecrawl-mcp
```

## 🚀 Usage

### Simple Agent
```bash
cd simple-agent
uv run main.py
```

**Example Queries:**
- "What is the pricing of Supabase?"
- "Extract the main features from the React documentation"
- "What are the latest updates on the OpenAI website?"

### Advanced Agent
```bash
cd advanced-agent
uv run main.py
```

**Example Queries:**
- "database hosting services"
- "CI/CD tools for Python"
- "monitoring solutions for web applications"

## 📁 Project Structure

```
AI-agents/
├── .gitignore                 # Git ignore rules
├── README.md                  # This file
├── simple-agent/             # Basic web scraping agent
│   ├── main.py              # Main entry point
│   ├── pyproject.toml       # Dependencies
│   └── .env                 # Environment variables
└── advanced-agent/          # Advanced research agent
    ├── main.py              # Main entry point
    ├── pyproject.toml       # Dependencies
    ├── .env                 # Environment variables
    └── src/                 # Source code
        ├── workflow.py      # LangGraph workflow
        ├── firecrawl.py     # Firecrawl service
        ├── models.py        # Pydantic models
        └── prompts.py       # LLM prompts
```

## 🔍 Key Components

### Simple Agent Components
- **MCP Integration**: Uses Model Context Protocol for tool access
- **Firecrawl MCP Server**: Provides web scraping capabilities
- **LangGraph Agent**: Orchestrates the conversation flow
- **Interactive Interface**: Real-time chat with the agent

### Advanced Agent Components
- **Research Workflow**: Multi-step process for tool analysis
- **Structured Data Models**: Pydantic models for consistent data
- **Company Analysis**: Automated extraction of developer-relevant information
- **Recommendation Engine**: AI-powered tool recommendations

## 🎯 Use Cases

### Simple Agent
- Quick web data extraction
- Real-time website monitoring
- Content analysis and summarization
- Research assistance

### Advanced Agent
- Developer tool research and comparison
- Technology stack analysis
- Pricing and feature comparison
- Development workflow optimization

## 🔒 Security

- API keys are stored in `.env` files (not committed to git)
- `.gitignore` prevents accidental exposure of sensitive data
- No hardcoded credentials in the codebase

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For issues and questions:
1. Check the existing issues
2. Create a new issue with detailed information
3. Include error messages and steps to reproduce

## 🔄 Updates

Both agents are designed to be easily extensible:
- Add new MCP tools to the simple agent
- Extend the research workflow in the advanced agent
- Customize prompts for specific use cases
- Add new data models for different types of analysis 