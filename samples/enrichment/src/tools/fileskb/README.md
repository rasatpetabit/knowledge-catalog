# FilesKB MCP Server

This is a simple MCP server for purposes of demonstrating how the enrichment
agent can be extended with MCP servers to access existing information sources.

The sample surfaces common file system capabilities - listing files, searching
files and reading files stored within a specified directory root.

## Using this MCP Server

The server can be provided to the agent using standard MCP configuration:

```json
{
  "mcpServers": {
    "fileskb": {
      "command": "${KC_ENRICH_SRC_DIR}/.venv/bin/python3",
      "args": [
        "${KC_ENRICH_SRC_DIR}/tools/fileskb/main.py",
        "--dir",
        "${KC_ENRICH_SAMPLE_DOCS_DIR}"
      ]
    }
  }
}
```
