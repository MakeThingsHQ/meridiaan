# LangChain and LangGraph

With [`langchain-mcp-adapters`](https://github.com/langchain-ai/langchain-mcp-adapters) (`pip install langchain-mcp-adapters`).

## LangChain: load the Workspace tools

```python
import asyncio
import os

from langchain_mcp_adapters.client import MultiServerMCPClient

client = MultiServerMCPClient(
    {
        "meridiaan-myproject": {
            "transport": "streamable_http",
            "url": "https://mcp.meridiaan.io/mcp/<workspace-id>",
            "headers": {"Authorization": f"Bearer {os.environ['MERIDIAAN_TOKEN']}"},
        }
    }
)


async def main() -> None:
    tools = await client.get_tools()
    print([tool.name for tool in tools])


asyncio.run(main())
```

## LangGraph: an agent on top of them

```python
from langgraph.prebuilt import create_react_agent


MODEL = "anthropic:<model-name>"  # or "openai:<model-name>", or a chat model object


async def ask(question: str) -> str:
    tools = await client.get_tools()
    agent = create_react_agent(MODEL, tools)
    result = await agent.ainvoke({"messages": [{"role": "user", "content": question}]})
    return result["messages"][-1].content
```

Use the model you prefer: the Workspace does not depend on it.

Status: not yet verified. [Report](../../../issues/new?template=client_report.yml) how it went.
