# Horizon plugin

Ask Horizon's Superconsultant about your organization from your AI tools: processes, findings,
discovery cycles and initiatives, answered from your own Horizon data.

Works in Cursor and Grok Bot (through the Cursor Marketplace) and in Grok Build.

## Requirements

A Horizon account with access to at least one company or workspace.

## Sign in

The first time a Horizon tool runs, your browser opens Horizon's sign-in page. Sign in with your
Horizon account and click **Allow**. No token or configuration file is needed.

The plugin sees exactly what you can see in Horizon: the same companies and workspaces.

## Configuration

None. The plugin declares no variables and needs no API key.

## Tools

| Tool | What it does |
|---|---|
| `get_prompting_guide` | Returns Horizon's guide to asking the Superconsultant well |
| `list_companies` | Lists the companies you can ask about |
| `list_workspaces` | Lists the workspaces you can reach inside one company |
| `superconsultant_ask` | Asks the Superconsultant a question about one company |

`superconsultant_ask` can change Horizon data when you ask it to (for example, creating an
initiative), and it can search the public web. The other three only read.

## Network access and credentials

- The plugin contains no code, hooks or scripts. It is one MCP server declaration.
- It calls one endpoint: `https://api.usehorizon.ai/mcp` (and Horizon's sign-in pages on
  `api.usehorizon.ai` and `app.usehorizon.ai` during OAuth).
- Credentials: none are stored in this repository or requested from you as text. The client
  obtains an OAuth token when you sign in and keeps it in its own credential store.
- No telemetry is sent by the plugin itself.

## Files

- `.cursor-plugin/plugin.json` and `mcp.json`: Cursor Marketplace (Cursor and Grok Bot).
- `.grok-plugin/plugin.json` and `.mcp.json`: Grok Build.

## License

MIT. See [LICENSE](LICENSE).

## Support

support@usehorizon.ai
