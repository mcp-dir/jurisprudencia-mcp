# Security Policy

O acesso ao Jurisprudência é via token (OAuth access_token ou JWT do agent-auth). **O token equivale a uma senha** — não compartilhe, não cole em chats públicos/issues/pastebins.

- Prefira **OAuth 2.1** quando o cliente suportar: o token nunca passa pelo chat.
- No fluxo **agent-auth**, o JWT passa pelo provedor LLM (Anthropic / OpenAI / Cursor) — ative retenção zero (Claude "Improve Claude" off, Cursor Privacy Mode) e rotacione.
- Este MCP **não move dinheiro nem altera dados** — é 100% leitura.

## Reportar vulnerabilidades

**NÃO abra issue pública.** Mande e-mail pra **[jurisprudencia@mcp.ai](mailto:jurisprudencia@mcp.ai)** com descrição, passos de reprodução e versão do cliente/SO. Resposta em até 72h úteis.
