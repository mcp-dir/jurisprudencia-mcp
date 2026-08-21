# Jurisprudência

### Jurisprudência for Claude, ChatGPT and AI agents

Case law search, court decisions and súmulas, across indexed public sources (STF, STJ, TST, state courts and Jusbrasil), by term or thesis, with title, snippet and link. Platform-hosted; no user credentials.

- 📊 **2 tools**
- 🔒 **Read-only**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Magic-link login (no password)**

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → name `Jurisprudência`, URL `https://api.mcp.ai/p_jurisprudencia`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=jurisprudencia&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9qdXJpc3BydWRlbmNpYSJ9)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=jurisprudencia&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_jurisprudencia%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_jurisprudencia
```

---

## 2 tools

| Tool | Description |
|---|---|
| `jurisprudencia_buscar` | Busca jurisprudência (acórdãos, súmulas, OJs) no acervo público LexML por termo/tese — cobre tribunais superiores e demais. |
| `jurisprudencia_sumulas` | Busca SÚMULAS (incluindo vinculantes) por termo no acervo LexML. |

---

## Pricing

Free.

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_jurisprudencia` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
