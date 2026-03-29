# MCP (Model Context Protocol) Bootcamp

## Project Overview

This is a hands-on MCP (Model Context Protocol) course project. It covers building and integrating MCP servers for AI applications using Python and TypeScript.

## Project Structure

- `binance_mcp/` - Python MCP server for Binance crypto price data
- `binance_mcp_reference_implementation/` - Reference implementation of the Binance MCP server (with prompt and resource variants)
- `typescript_mcp/` - TypeScript MCP server implementation of the same Binance price tool
- `langgraph/` - LangGraph agent that uses the MCP server via LangChain adapters
- `mcp_client.py` - Simple MCP client example
- `tool_calling.ipynb` - Jupyter notebook for interactive exploration
- `ref-*/` - Reference implementations (Docker, Cloudflare, OpenAI, etc.)
- `_extra_resources/` - Additional course resources

## Tech Stack

- **Language**: Python 3.11, Node.js 20 / TypeScript
- **Package Manager**: `uv` (Python), `npm` (TypeScript)
- **Key Libraries**: `mcp[cli]`, `langchain`, `langgraph`, `langchain-mcp-adapters`, `google-generativeai`
- **Jupyter**: JupyterLab / Notebook for interactive exploration

## Running the Project

The main workflow starts a JupyterLab server on port 5000, which serves all notebooks and allows running scripts interactively.

```
uv run jupyter notebook --ip=0.0.0.0 --port=5000 --no-browser --NotebookApp.token='' --NotebookApp.password=''
```

## Environment Variables

Configured in `.env` (copy `.env.example` if needed):
- `GEMINI_API_KEY` - Google Gemini API key
- `OPENAI_API_KEY` - OpenAI API key
- `LANGSMITH_TRACING` / `LANGSMITH_ENDPOINT` / `LANGSMITH_API_KEY` / `LANGSMITH_PROJECT` - LangSmith tracing (optional)

## Building the TypeScript MCP Server

```bash
cd typescript_mcp
npm install
npm run build
```

## Running Python Scripts

Use `uv run` to execute scripts within the virtual environment:

```bash
uv run python mcp_client.py
uv run python langgraph/price_graph.py
```
