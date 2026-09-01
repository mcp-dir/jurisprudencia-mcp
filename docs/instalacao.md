# Instalação detalhada

Jurisprudência é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_jurisprudencia`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_jurisprudencia` | nenhuma (grátis) |
| Cursor | `https://api.mcp.ai/p_jurisprudencia` | nenhuma |
| VS Code (Copilot) | `https://api.mcp.ai/p_jurisprudencia` | nenhuma |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.jurisprudencia` (ou `servers.jurisprudencia` no VS Code) do config do cliente e reinicie.
