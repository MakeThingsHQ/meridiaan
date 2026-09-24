# Python

With the official MCP SDK (`pip install mcp`). The SDK is asynchronous.

```python
import asyncio
import os

from mcp import ClientSession
from mcp.client.streamable_http import streamablehttp_client

URL = "https://mcp.meridiaan.io/mcp/<workspace-id>"
HEADERS = {"Authorization": f"Bearer {os.environ['MERIDIAAN_TOKEN']}"}


async def main() -> None:
    async with streamablehttp_client(URL, headers=HEADERS) as (read, write, _):
        async with ClientSession(read, write) as session:
            await session.initialize()

            tools = await session.list_tools()
            print([tool.name for tool in tools.tools])

            info = await session.call_tool("get_workspace_informations", {})
            print(info.content[0].text)


asyncio.run(main())
```

`get_workspace_informations` returns the Workspace description and its Collections, with the id each read or write needs.

Status: not yet verified. [Report](../../../issues/new?template=client_report.yml) how it went.
