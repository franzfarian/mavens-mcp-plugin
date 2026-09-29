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
