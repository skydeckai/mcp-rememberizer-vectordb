# MCP Get Community Servers

TODO: Add description

## Components

### Resources

The server provides access to two types of resources: Documents or Slack discussions

### Tools

TODO: Add tools

## Installation

### Using uv (recommended)

When using [`uv`](https://docs.astral.sh/uv/), no specific installation is needed. Use [`uvx`](https://docs.astral.sh/uv/guides/tools/) to directly run _mcp-rememberizer-vectordb_.

## Configuration

### Environment Variables

The following environment variables are required:

- `REMEMBERIZER_VECTOR_STORE_API_KEY`: Your Rememberizer Vector Store API token

You can register an API key by create your own [Vector Store in Rememberizer](https://docs.rememberizer.ai/developer/vector-stores).

### Usage with Claude Desktop

Add this to your `claude_desktop_config.json`:

```json
"mcpServers": {
  "rememberizer": {
      "command": "uvx",
      "args": ["mcp-rememberizer-vectordb"],
      "env": {
        "REMEMBERIZER_VECTOR_STORE_API_KEY": "your_rememberizer_api_token"
      }
    },
}
```

## Debugging

Since MCP servers run over stdio, debugging can be challenging. For the best debugging
experience, we strongly recommend using the [MCP Inspector](https://github.com/modelcontextprotocol/inspector).

You can launch the MCP Inspector via [`npm`](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) with this command:

```bash
npx @modelcontextprotocol/inspector uv --directory /path/to/directory/mcp-rememberizer-vectordb/src/mcp_rememberizer_vectordb run mcp-rememberizer-vectordb
```

Upon launching, the Inspector will display a URL that you can access in your browser to begin debugging.

## License

This MCP server is licensed under the MIT License. This means you are free to use, modify, and distribute the software, subject to the terms and conditions of the MIT License. For more details, please see the LICENSE file in the project repository.
