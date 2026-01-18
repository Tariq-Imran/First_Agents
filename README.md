
LangChain Essentials!



🚀 Setup

Browser

The Brave browser is recommended

Prerequisites

Ensure you're using Python 3.11 - 3.13. This version is required for optimal compatibility with LangChain
uv package manager or pip
Set up LLM API Keys

You'll need an OpenAI API key. If you don’t have an OpenAI API key, you can sign up here.

Install Node.js

You'll need Node.js and npx (required for MCP server in notebook 3).


# Verify installation:
node --version
npx --version

Sign up for LangSmith

Create a LangSmith account and API key 


# Add your API key to your .env file
LANGSMITH_API_KEY=your_langsmith_api_key_here
LANGSMITH_TRACING=true
LANGSMITH_PROJECT=langchain-py-essentials
# If you are on the EU instance:
LANGSMITH_ENDPOINT=https://eu.api.smith.langchain.com

Installation

Download the course repository:

# Clone the repo, cd to 'python' directory
git clone https://github.com/langchain-ai/lca-langchainV1-essentials.git


Make a copy of example.env:

# Create .env file
cp example.env .env
Insert API keys directly into .env file, OpenAI (required) and LangSmith (optional):

# Add OpenAI API key
OPENAI_API_KEY=your_openai_api_key_here
# The course is written using OpenAI models. You can choose other vendors if you prefer.
# Remember to change the code and add their key.
#ANTHROPIC_API_KEY=anthropic_api_key_here_if_you_prefer

# Optional API key for LangSmith tracing
LANGSMITH_API_KEY=your_langsmith_api_key_here
LANGSMITH_TRACING=true
LANGSMITH_PROJECT=langchain-py-essentials
Make a virtual environment and install dependencies:

# Create virtual environment and install dependencies
uv sync
Run notebooks:

# Run Jupyter notebooks directly with uv
uv run jupyter lab

# Or activate the virtual environment if preferred
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
jupyter lab
Optional: Setup LangSmith Studio

# copy the .env file you created above to the studio directory
cp .env ./studio/.
cd studio

#to run with uv
uv run langgraph dev
#to run with virtual env
langgraph dev


📚 Lessons

This repository contains nine short notebooks that serve as brief introductions to many of the most-used features in LangChain, starting with the new Create Agent.

L1_fast_agent.ipynb - 🤖 Create Agent 🤖

In this notebook, you will use LangChain’s create_agent to build an SQL agent in just a few lines of code.
It demonstrates how quick and easy it is to build a powerful agent. You can easily take this agent and apply it to your own project.
You will also use LangSmith Studio, a handy visual debugger to run, host, and explore agents.

L2-7.ipynb - 🧱 Building Blocks 🧱

In Lessons 2–7, you will learn how to use some of the fundamental building blocks in LangChain. These lessons explain and complement create_agent, and you’ll find them useful when creating your own agents. Each lesson is concise and focused.

L2_messages.ipynb: Learn how messages convey information between agent components.
L3_streaming.ipynb: Learn how to reduce user-perceived latency using streaming.
L4_tools.ipynb: Learn basic tool use to enhance your model with custom or prebuilt tools.
L5_tools_with_mcp.ipynb: Learn to use the LangChain MCP adapter to access the world of MCP tools.
L6_memory.ipynb: Learn how to give your agent the ability to maintain state between invocations.
L7_structuredOutput.ipynb: Learn how to produce structured output from your agent.
L8-9.ipynb - 🪛 Customize Your Agent 🤖

Lessons 2–7 covered out-of-the-box features. However, create_agent also supports both prebuilt and user-defined customization through Middleware. This section describes middleware and includes two lessons highlighting specific use cases.

L8_dynamic.ipynb: Learn how to dynamically modify the agent’s system prompt to react to changing contexts.
L9_HITL.ipynb: Learn how to use Interrupts to enable Human-in-the-Loop interactions.