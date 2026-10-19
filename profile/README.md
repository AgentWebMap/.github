<p align="center">
  <a href="https://agentwebmap.com"><picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://agentwebmap.com/logo-dark.svg">
    <img src="https://agentwebmap.com/logo.svg" alt="Agent Web Map" width="420">
  </picture></a>
</p>

<p align="center"><strong>The map of the agent-readable web.</strong><br>
A directory of websites that publish <a href="https://llmstxt.org/">llms.txt</a>, validated and ranked by authority, with a free JSON API and an MCP server for AI agents.</p>

<p align="center">
  <a href="https://agentwebmap.com">Website</a> ·
  <a href="https://agentwebmap.com/docs">API docs</a> ·
  <a href="https://agentwebmap.com/docs#mcp">MCP server</a> ·
  <a href="https://agentwebmap.com/llms.txt">llms.txt</a> ·
  <a href="https://agentwebmap.com/map">World map</a> ·
  <a href="https://agentwebmap.com/check">Check your llms.txt</a> ·
  <a href="https://agentwebmap.com/generate">Generate one</a>
</p>

## For agents

One call returns the best source for a domain or a topic, with what to read, the owner's terms for agents, health and alternatives:

```
GET https://agentwebmap.com/v1/resolve?q=stripe.com
GET https://agentwebmap.com/v1/resolve?q=payments+api
```

`GET https://agentwebmap.com/v1` lists everything else. Reads need no key. Any domain page answers in JSON or Markdown through the `Accept` header, and `POST /v1/watch` tells you, signed, when a site's llms.txt changes or breaks.

Add the MCP server to Claude Code:

```bash
claude mcp add --transport http agentwebmap https://agentwebmap.com/mcp
```

or to any client that takes a JSON config:

```json
{ "mcpServers": { "agentwebmap": { "url": "https://agentwebmap.com/mcp" } } }
```

## For site owners

Publish an llms.txt, then two calls with no account: `POST /v1/sites` to register, place the token, `POST /v1/sites/<domain>/verify`. Verified owners rank first, are featured sooner, get a badge, breakage alerts, analytics, and can publish their terms for agents. Not sure your file is right? [Check it](https://agentwebmap.com/check). Don't have one? [Generate a draft](https://agentwebmap.com/generate).

## Repositories

- [mcp](https://github.com/AgentWebMap/mcp): the MCP server description, tool list and setup.

Contact: admin@agentwebmap.com
