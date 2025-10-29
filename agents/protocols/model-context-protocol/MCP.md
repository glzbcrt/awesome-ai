# Model Context Protocol

## Specification

- [Model Context Protocol](https://modelcontextprotocol.io)
- [Model Context Protocol - GitHub Organization](https://github.com/modelcontextprotocol)
- [Specification Enhancement Proposal (SEP) guidelines](https://modelcontextprotocol.io/community/sep-guidelines)

## General

- [Introducing the Model Context Protocol](https://www.anthropic.com/news/model-context-protocol)
- [MCP Dev Days: Day 1 - DevTools](https://www.youtube.com/watch?v=8-okWLAUI3Q)
- [MCP Dev Days: Day 2 - Builders](https://www.youtube.com/watch?v=lHuxDMMkGJ8)
- [How to build secure and scalable remote MCP servers](https://github.blog/ai-and-ml/generative-ai/how-to-build-secure-and-scalable-remote-mcp-servers/)

## Clients

- [Example Clients](https://modelcontextprotocol.io/clients)

## Servers

- [Microsoft MCP Servers](https://github.com/microsoft/mcp)
- [Microsoft MCP Center ](https://mcp.azure.com/)
- [GitHub MCP Server](https://github.com/github/github-mcp-server)
- [SQL Server MCP Server](https://github.com/Azure-Samples/SQL-AI-samples/tree/main/MssqlMcp/dotnet)
- [Docker mcp Servers](https://hub.docker.com/u/mcp)

### Reference MCP Servers for Common Scenarios

- [Model Context Protocol servers](https://github.com/modelcontextprotocol/servers)
- [Everything MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/everything)
- [Filesystem MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem)

## Videos

- [Next Generation Agent Architectures with MCP with Darren Shepherd from Acorn Labs](https://www.youtube.com/watch?v=z4vgc3lFMYM)
- [Intro to OAuth for MCP Servers with Aaron Parecki, Okta](https://www.youtube.com/watch?v=mYKMwZcGynw)
- [Remote MCPs: What we learned from shipping — John Welsh, Anthropic](https://www.youtube.com/watch?v=0NHCyq8bBcM)
- [Multi Agent Collaboration in MCP with Nicholas Aldridge from AWS](https://www.youtube.com/watch?v=XreKuebKpaA)
- [[Keynote] MCP201: The Protocol in Depth with David Soria Parra at Anthropic](https://www.youtube.com/watch?v=C_nqAWHsldo)
- [Building with MCP and the Claude API](https://www.youtube.com/watch?v=aZLr962R6Ag)

## MCP-UI

- [MCP-UI](https://mcpui.dev/)
- [[Session] MCP-UI: Next-gen Agentic Experiences](https://www.youtube.com/watch?v=SIXTArBVL5w)

## Tools

### MCP Inspector

- [Source code](https://github.com/modelcontextprotocol/inspector)

#### One Line Commands

```pwsh
npx @modelcontextprotocol/inspector --server-url http://localhost:7072
```

### MCP Server Everything

- [Source code](https://github.com/modelcontextprotocol/servers/tree/main/src/everything)

#### One Line Commands

```pwsh
npx @modelcontextprotocol/server-everything
```

## Libraries

- [MCP TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk)
- [MCP C# SDK](https://github.com/modelcontextprotocol/csharp-sdk)
- [MCP Go SDK](https://github.com/modelcontextprotocol/go-sdk)

### Python

- [MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk)
- [FastMCP](https://gofastmcp.com)

## Security

- [MCP Vulnerabilities Every Developer Should Know](https://composio.dev/blog/mcp-vulnerabilities-every-developer-should-know)

### Tool Poisoning

- [MCP Security Notification: Tool Poisoning Attacks](https://invariantlabs.ai/blog/mcp-security-notification-tool-poisoning-attacks)
- [Protecting against indirect prompt injection attacks in MCP](https://devblogs.microsoft.com/blog/protecting-against-indirect-injection-attacks-mcp)
- [Prevent MCP Tool Poisoning With a Registration Workflow](https://www.solo.io/blog/prevent-mcp-tool-poisoning-with-registration-workflow)
- [Introducing MCP-Scan: Protecting MCP with Invariant](https://invariantlabs.ai/blog/introducing-mcp-scan)
- [WhatsApp MCP Exploited: Exfiltrating your message history via MCP](https://invariantlabs.ai/blog/whatsapp-mcp-exploited)
- [Poison everywhere: No output from your MCP server is safe](https://www.cyberark.com/resources/threat-research-blog/poison-everywhere-no-output-from-your-mcp-server-is-safe)
- [Let's talk about "Tool Poisoning"](https://www.epicai.pro/lets-talk-about-tool-poisoning)

### OAuth Authentication

- [Evolving OAuth Client Registration in the Model Context Protocol](https://blog.modelcontextprotocol.io/posts/client_registration/)
- [SEP-991: Enable URL-based Client Registration using OAuth Client ID Metadata Documents](https://github.com/modelcontextprotocol/modelcontextprotocol/issues/991)
- [SEP-1032: Support software_statement and jwks_uri in Dynamic Client Registration for MCP](https://github.com/modelcontextprotocol/modelcontextprotocol/issues/1032)
- [RFC6749 - The OAuth 2.0 Authorization Framework](https://datatracker.ietf.org/doc/html/rfc6749)
- [RFC9728 - OAuth 2.0 Protected Resource Metadata](https://datatracker.ietf.org/doc/html/rfc9728/)
- [RFC8615 - Well-Known Uniform Resource Identifiers (URIs)](https://datatracker.ietf.org/doc/html/rfc8615)
- [RFC8414 - OAuth 2.0 Authorization Server Metadata](https://datatracker.ietf.org/doc/html/rfc8414)
- [What is Dynamic Client Registration?](https://www.descope.com/learn/post/dynamic-client-registration)
- [RFC7591 - OAuth 2.0 Dynamic Client Registration Protocol](https://datatracker.ietf.org/doc/html/rfc7591)

#### Videos

- [AWS re:Inforce 2025 - Secure remote MCP server deployment for Gen AI on AWS (SEC326)](https://www.youtube.com/watch?v=lC2dLQZAlo8)
- [How to Secure Agents using OAuth — Jared Hanson (Keycard, Passport.js)](https://www.youtube.com/watch?v=blmAkayzE8M)

## One line requests for STDIO servers

**Initialize Session**

```json
{"jsonrpc":"2.0","id":1,"method":"initialize","params":{"protocolVersion":"2024-11-05","capabilities":{"roots":{"listChanged":true},"sampling":{},"elicitation":{}},"clientInfo":{"name":"ExampleClient","title":"Example Client Display Name","version":"1.0.0"}}}
```

**List the tools available**

```json
{"jsonrpc":"2.0","id":2,"method":"tools/list","params":{"cursor":"optional-cursor-value"}}
```

**Execute tool**

```json
{"jsonrpc":"2.0","id":3,"method":"tools/call","params":{"name":"summarize","arguments":{"text":"Hello World from Microsoft!"}}}
```

**Sampling Response**

```json
{"jsonrpc":"2.0","id":1,"result":{"role":"assistant","content":{"type":"text","text":"The capital of France is Paris."},"model":"claude-3-sonnet-20240307","stopReason":"endTurn"}}
```json
 