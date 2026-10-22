<p align="center"><a href="https://agentwebmap.com/"><picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://agentwebmap.com/logo-dark.svg?v=awm-20261022">
  <img src="https://agentwebmap.com/logo.svg?v=awm-20261022" alt="Agent Web Map" width="420">
</picture></a></p>

# Find the next useful source for your agent

[Agent Web Map](https://agentwebmap.com/) discovers and continuously validates websites publishing llms.txt. People can browse publishers and explore their shared headings; AI agents can find original source links through the free JSON API and hosted MCP server.

[Try a real task lookup](https://agentwebmap.com/#task-discovery): enter a publisher and task, inspect matching evidence and check dates, then read the original pages. [Connect your agent](https://agentwebmap.com/docs#start) for repeated use through HTTP or MCP. Connections expose tools; the client decides when to use them.

**[Browse and search](https://agentwebmap.com/browse) · [Explore sections](https://agentwebmap.com/explore) · [Statistics](https://agentwebmap.com/stats) · [API & MCP](https://agentwebmap.com/docs)**

## For people

Use the clean text-file interface in light or dark mode, with sans-serif text and monospace headings and code. [Sign in with an email code](https://agentwebmap.com/workspace/signin) to save favorite sources, organize private collections and revisit recently opened references. Your workspace is private; the directory and agent tools stay open without an account.

- Start with [curated source collections](https://agentwebmap.com/collections), or [make your own](https://agentwebmap.com/workspace/collections).

- Find a publisher or documentation for a task in [Browse](https://agentwebmap.com/browse).
- Explore connections between headings across files in the growing [section cloud](https://agentwebmap.com/explore).
- The point cloud measures shared publisher headings. Meaning-based search and inferred topic categories provide separate discovery signals.
- See current counts, growth and file statistics in [Statistics](https://agentwebmap.com/stats), or explore the [world map](https://agentwebmap.com/map).
- [Check your llms.txt](https://agentwebmap.com/check), [generate a draft](https://agentwebmap.com/generate), or [submit a site](https://agentwebmap.com/submit).

## For agents and integrations

Connect an HTTP MCP client to **`https://agentwebmap.com/mcp`**, or start with [the REST API](https://agentwebmap.com/v1). Public discovery needs no account or API key.

The 20 hosted MCP tools cover task resolution, publisher search and lookup, cached-file reads, categories, countries, section connections, validation, generation and optional owner management. Keyword and meaning-based search rank task relevance first. The client chooses when to call the available tools.

[Country filtering](https://agentwebmap.com/docs#countries) works in Browse, the section cloud, REST and MCP: use `country=FR` or `country=unknown`, and discover available codes with [`GET /v1/countries`](https://agentwebmap.com/v1/countries) or `list_countries`. Location is inferred from domains or hosting, not verified business headquarters or markets served.

**[Client setup and tool list](https://github.com/AgentWebMap/mcp#add-it) · [API documentation](https://agentwebmap.com/docs) · [Markdown docs](https://agentwebmap.com/docs.md) · [OpenAPI](https://agentwebmap.com/openapi.json)**

Try a task lookup: [Model Context Protocol authorization](https://agentwebmap.com/v1/resolve?q=modelcontextprotocol%20authorization). For headings, start with [`/v1/sections`](https://agentwebmap.com/v1/sections), then explore connections with [`/v1/section-graph`](https://agentwebmap.com/v1/section-graph).

Public discovery is monitored without automatic daily usage or pagination quotas. [Access details](https://agentwebmap.com/docs#limits).

## For website owners

[Verify your website—free](https://agentwebmap.com/verify?from=github) to control its profile and terms for agents, recheck file health, and return to a private dashboard with daily discovery activity and score history. [Preview the dashboard](https://agentwebmap.com/manage/preview). Valid, listed, unblocked, verified profiles are eligible for search-engine visibility. Eligible verified publishers are named in [our llms-full.txt](https://agentwebmap.com/llms-full.txt); default Browse places verified listings first while task search prioritizes relevance. Verified listings receive an ownership signal and an embeddable badge. No backlink is required.

Sites can be discovered automatically; verification is optional for inclusion. It confirms domain control rather than content accuracy. [Ownership guide](https://github.com/AgentWebMap/mcp/blob/main/docs/ownership.md).

## Learn about llms.txt

[What is llms.txt?](https://agentwebmap.com/what-is-llms-txt) · [Real examples](https://agentwebmap.com/llms-txt-examples) · [Best practices](https://agentwebmap.com/llms-txt-best-practices) · [About the directory](https://agentwebmap.com/about)

Coverage is incomplete. Read the original publisher pages before relying on an answer. Indexed headings and declared endpoints are discovery signals, not proof of an available action. Usage totals can include bots and repeated requests.

[The public repository](https://github.com/AgentWebMap/mcp) contains the platform introduction and integration documentation. The hosted application is maintained separately.

[Contact us](https://agentwebmap.com/contact) · [X](https://x.com/AgentWebMap) · [Agent-readable overview](https://agentwebmap.com/llms.txt)

Updated 22 October 2026.
