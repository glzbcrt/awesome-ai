# Model Context Protocol

## Specification

- [Model Context Protocol](https://modelcontextprotocol.io)
- [Model Context Protocol - GitHub Organization](https://github.com/modelcontextprotocol)

## General

- [Introducing the Model Context Protocol](https://www.anthropic.com/news/model-context-protocol)
- [MCP Dev Days: Day 1 - DevTools](https://www.youtube.com/watch?v=8-okWLAUI3Q)
- [MCP Dev Days: Day 2 - Builders](https://www.youtube.com/watch?v=lHuxDMMkGJ8)

## Servers

- [Everything MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/everything)

## Tools

- [MCP Inspector](https://github.com/modelcontextprotocol/inspector)

## Libraries

- [MCP TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk)

## Security

### Tool Poisoning

- [MCP Security Notification: Tool Poisoning Attacks](https://invariantlabs.ai/blog/mcp-security-notification-tool-poisoning-attacks)
- [Protecting against indirect prompt injection attacks in MCP](https://devblogs.microsoft.com/blog/protecting-against-indirect-injection-attacks-mcp)
- [Prevent MCP Tool Poisoning With a Registration Workflow](https://www.solo.io/blog/prevent-mcp-tool-poisoning-with-registration-workflow)
- [Introducing MCP-Scan: Protecting MCP with Invariant](https://invariantlabs.ai/blog/introducing-mcp-scan)
- [WhatsApp MCP Exploited: Exfiltrating your message history via MCP](https://invariantlabs.ai/blog/whatsapp-mcp-exploited)
- [Poison everywhere: No output from your MCP server is safe](https://www.cyberark.com/resources/threat-research-blog/poison-everywhere-no-output-from-your-mcp-server-is-safe)
- [Let's talk about "Tool Poisoning"](https://www.epicai.pro/lets-talk-about-tool-poisoning)

## One Line Requests

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
 