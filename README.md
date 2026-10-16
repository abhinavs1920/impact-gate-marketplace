# Impact Gate marketplace

Official Claude Code plugin marketplace for [Impact Gate](https://impactgate.in) - read-only API change impact evidence for AI coding assistants.

The plugin connects Claude Code to the hosted Impact Gate MCP server and adds six read-only tools: workspace status, change analysis, consumer lookup, API flow detail, function usage, and fix verification. Every answer is scoped to workspaces your Google account is authorized for, with the indexed commit and freshness attached.

## Install

```bash
claude plugin marketplace add abhinavs1920/impact-gate-marketplace
claude plugin install impact-gate@impact-gate-marketplace
```

On first use, your browser opens the Impact Gate consent page. Sign in with Google (the same account as your Impact Gate workspace) to authorize the `impact:read` scope. No API keys.

## Just the MCP URL

Any MCP client can connect directly without the plugin:

```text
https://mcp.impactgate.in/
```

- Claude (web/desktop): Settings > Connectors > Add custom connector, paste the URL. Works on the Free plan.
- Claude Code: `claude mcp add --transport http impact-gate https://mcp.impactgate.in/`
- Cursor / VS Code: add `{ "url": "https://mcp.impactgate.in/" }` as an HTTP MCP server.

Full setup guides: [Connect an AI client](https://impactgate.in/docs/connect-mcp-clients)

## Docs

- [Impact Gate MCP server](https://impactgate.in/docs/mcp-server) - how sign-in works, scoping, errors, security
- [MCP tools reference](https://impactgate.in/docs/mcp-tools) - parameters and examples for the six tools
- [Terms of Service](https://impactgate.in/docs/terms-of-service)

## Contact

contact@impactgate.in
