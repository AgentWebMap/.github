<p align="center">
  <a href="https://agentwebmap.com"><picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://agentwebmap.com/logo-dark.svg">
    <img src="https://agentwebmap.com/logo.svg" alt="Agent Web Map" width="420">
  </picture></a>
</p>

<p align="center"><strong>Find publisher documentation for your agent's next task.</strong><br>
AgentWebMap indexes websites publishing <a href="https://llmstxt.org/">llms.txt</a> and helps AI agents find relevant documentation through a free API and MCP server, with original source links, matching evidence and freshness information.</p>

<p align="center">
  <a href="https://agentwebmap.com/discover">Try discovery</a> ·
  <a href="https://agentwebmap.com/coverage">Coverage</a> ·
  <a href="https://agentwebmap.com/contact">Contact us</a> ·
  <a href="https://agentwebmap.com/benchmarks">Benchmarks</a> ·
  <a href="https://x.com/AgentWebMap">X</a> ·
  <a href="https://agentwebmap.com/docs">API docs</a> ·
  <a href="https://agentwebmap.com/docs#mcp">MCP server</a> ·
  <a href="https://agentwebmap.com/llms.txt">llms.txt</a> ·
  <a href="https://agentwebmap.com/check">Check your llms.txt</a> ·
  <a href="https://agentwebmap.com/generate">Generate one</a>
</p>

## Use it for a task

One call finds documentation links for a domain or development task, with publisher-provided matching evidence, freshness, owner terms and alternatives:

```
GET https://agentwebmap.com/v1/resolve?q=modelcontextprotocol.io
GET https://agentwebmap.com/v1/resolve?q=modelcontextprotocol+authorization&limit=3&max_age=86400
```

`GET https://agentwebmap.com/v1` lists everything else. Reads need no key. Any domain page answers in JSON or Markdown through the `Accept` header, and `POST /v1/watch` tells you, signed, when a site's llms.txt changes or breaks.

Add the MCP server to Codex:

```bash
codex mcp add agentwebmap --url https://agentwebmap.com/mcp
```

Or to Claude Code:

```bash
claude mcp add --transport http agentwebmap https://agentwebmap.com/mcp
```

Cursor and VS Code also use the same HTTP endpoint. Their configuration keys differ: Cursor uses `mcpServers` in `.cursor/mcp.json`; VS Code uses `servers` in `.vscode/mcp.json`. See [client-specific setup](https://github.com/AgentWebMap/mcp#add-it) for exact configurations, including user and project paths for all four clients.

For dependency-aware discovery, run the [Node.js CLI](https://github.com/AgentWebMap/mcp/blob/main/docs/discovery-cli.md) from a repository checkout:

```bash
node examples/discover.mjs --project /path/to/project --dry-run
node examples/discover.mjs --project /path/to/project
```

The preview shows recognized dependency-to-publisher mappings without network calls or writes. The normal run makes a small, bounded set of index requests and prints JSON with source evidence and freshness. No package install, project execution, or automatic instruction-file edits are needed.

Coverage is incomplete. Read the original documentation before relying on it: the index searches published llms.txt link descriptions and headings, not the full text of every linked page. Missing, weak or stale results need the publisher's own search or web search. The optional [discovery skill](https://github.com/AgentWebMap/mcp/tree/main/skills/agentwebmap-docs), [task examples](https://github.com/AgentWebMap/mcp/blob/main/docs/task-examples.md) and [benchmark runner](https://github.com/AgentWebMap/mcp/tree/main/benchmarks) make the workflow reusable and measurable. Connecting MCP makes tools available; the agent client chooses when to use them.

Use `GET /v1/categories` or the `list_categories` MCP tool to discover category filters for providers. Labels are inferred by versioned rules from publisher metadata, with evidence in full domain responses; uncategorized means the evidence was insufficient. Separately, `capability=mcp` finds explicit publisher-declared endpoint links; availability and tools remain unverified. [Category reference](https://github.com/AgentWebMap/mcp/blob/main/docs/categories.md).

## For site owners

Sites are discovered from public llms.txt files and can be used by agents immediately. Inclusion does not imply endorsement, partnership or publisher participation. Owners can optionally [manage their listing in the browser](https://agentwebmap.com/manage) to edit information, publish terms for agents, configure breakage alerts and see measured discovery requests and publisher clicks. No terminal or backlink is required.

The [ownership guide](https://github.com/AgentWebMap/mcp/blob/main/docs/ownership.md) covers secure browser, API and MCP management, fresh ownership challenges and key recovery.

Task searches rank relevance first; ownership confirmation proves domain control rather than content accuracy. Usage counts can include bots, tests and repeated calls; they do not measure unique agents or confirmed reads. Not sure your file is right? [Check it](https://agentwebmap.com/check). Don't have one? [Generate a draft](https://agentwebmap.com/generate).

## Repositories

- [mcp](https://github.com/AgentWebMap/mcp): MCP client setup, free API reference, runnable examples, dependency-aware CLI and optional discovery skill.

Want to evaluate or describe the project? Start with the [coverage report](https://agentwebmap.com/coverage), then use the [listing copy and adoption checklist](https://github.com/AgentWebMap/mcp/blob/main/docs/distribution.md). Directory size, curated benchmark results, observed requests and independent agent adoption measure different things.

Contact: admin@agentwebmap.com
