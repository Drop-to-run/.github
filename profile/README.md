## Drop2Run

**Publishing for what AI makes.**

A page your AI wrote, a folder of documents, a built site — each becomes an HTTPS link anyone can
open, in seconds. Publish from a chat, a coding agent, a shell or a browser drop. No account, no build
step, no git.

### Built for agents

- **A Claude connector.** Drop2Run is in
  [Claude's connector directory](https://claude.ai/directory/connectors/drop2run). Connect it once,
  sign in with your account, and "put this online" ends in a URL, with nothing to install.
- **A full MCP server, hosted or local.** The same tools, at `https://mcp.dropto.run/mcp` or through
  `npx @drop2run/mcp`, for Claude, ChatGPT, Cursor, VS Code, Codex, Gemini CLI or any MCP client. An
  agent can do more than publish:
  - update a site's settings;
  - roll back to an earlier version;
  - pause and resume a site;
  - change its address;
  - invite people;
  - read and answer comments.
- **A CLI that runs headless.** `drop2run` works in a shell, in CI or in a container. It ships with a
  [SKILL.md](https://dropto.run/SKILL.md), so a coding agent knows which command to run without being
  told.

### Comments, with the agent in the loop

Share a site for review, and the people you invite pin comments to the page: on a point of an HTML
page, or on words selected in a Markdown, code or text file. Comments arrive live, with an email digest. The owner
answers on the page, or an agent reads the threads over MCP, fixes the source, publishes, and replies.
Hosting and review happen in one place, with no snippet or extension to install. Comments are
available on plans that include them.

### Real hosting underneath

- **Documents open in a reader.** That covers Markdown with Mermaid and KaTeX, PDF, Word, Excel, EPUB,
  and CSV as a table. The same URL returns the raw file to `curl` or an agent.
- **Hosting features.** Sites are served from Cloudflare's edge in 300+ cities, with:
  - custom domains;
  - passwords and invite-only sites;
  - versions and rollback;
  - `_redirects` rules;
  - an `/api/*` proxy that keeps your API key out of the browser.
- **Pricing.** Publishing is free, with or without an account, and traffic is never billed.

```bash
# From Claude Code, through the hosted MCP server
claude mcp add --transport http drop2run https://mcp.dropto.run/mcp

# From a shell
npm i -g drop2run
drop2run deploy dist
```

**[dropto.run](https://dropto.run)** · [Docs](https://dropto.run/docs) ·
[Connect an agent](https://dropto.run/docs/agents) · [Changelog](https://dropto.run/changelog) ·
[drop2run-cli](https://github.com/Drop-to-run/drop2run-cli) (source for the CLI and the MCP server)
