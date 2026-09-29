# MAVENS.mcp for Cursor

Review connected software projects and read findings with MAVENS.

## Connect

Install this plugin in Cursor, enable the MAVENS MCP server, and sign in to your MAVENS account when Cursor opens the OAuth flow. The endpoint is `https://mavens.it/api/mcp`. No API key is included or required in the configuration.

For manual setup, merge the `mavens` entry from `mcp.json` into your Cursor MCP configuration. Keep your other server entries.

## Try it

- “Show my MAVENS connection status and available repositories.”
- “Explain how to request a MAVENS project review.”
- “Show the latest review findings for my connected project.”

## Tools and review approval

MAVENS exposes `mavens_help`, `mavens_status`, `mavens_repositories`, `mavens_remote_review`, `mavens_latest_scan`, and `mavens_submit_scan`. Use the server's current tool schemas and instructions.

A remote review requires an admitted repository and explicit approval of the exact repository, commit, report recipient and review scope. Recipient verification may be required. Connecting alone does not run a review. Remote reviews access the approved repository through the MAVENS review runner.

Structured results from an authorized MAVENS Local review can also be submitted. Do not put source code or secrets into tool arguments. Repositories and results are scoped to the signed-in account. Report actual scanner failures and incomplete checks; do not describe them as a clean security assessment.

## Local plugin test

Copy this plugin folder under `~/.cursor/plugins/local/mavens-mcp`, reload Cursor, and confirm the MAVENS server appears in Customize. Authenticate, then call help and status. Review actions remain subject to their own approval flow.

## Links

- [Documentation](https://mavens.it/mcp/)
- [Privacy policy](https://mavens.it/en/privacy-policy/)
- [Service terms](https://mavens.it/en/terms-of-service/)
- Support: hamburg@mavens.de

## License

The plugin configuration and documentation are MIT licensed. The MAVENS name and logo remain trademarks of MAVENS GmbH. The hosted MAVENS service is governed by its service terms.

## VS Code

Run **MCP: Add Server** from the Command Palette, choose **HTTP**, and enter `https://mavens.it/api/mcp`. Name it `MAVENS.mcp` and complete the MAVENS OAuth sign-in.

Equivalent `.vscode/mcp.json` configuration:

```json
{"servers":{"MAVENS.mcp":{"type":"http","url":"https://mavens.it/api/mcp"}}}
```

## Replit

[Add MAVENS.mcp to Replit](https://replit.com/integrations?mcp=eyJkaXNwbGF5TmFtZSI6Ik1BVkVOUy5tY3AiLCJiYXNlVXJsIjoiaHR0cHM6Ly9tYXZlbnMuaXQvYXBpL21jcCJ9). Complete OAuth when prompted. This link adds a personal connection; public catalog availability is managed separately by Replit.

## v0

In v0's MCP integrations, add a custom server with `https://mavens.it/api/mcp` and complete OAuth. The connection provides tools to the v0 agent; it does not add the MAVENS integration to your generated application's runtime.

## Registry metadata

`server.json` describes the hosted server for the official MCP Registry. This repository contains public connection configuration and documentation; the hosted service's application source is not distributed here. Registry metadata is published manually from `main` using GitHub OIDC, with no stored publishing secret. A registry publication does not imply approval by every downstream catalog.
