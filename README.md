# Jurisprudência

### Jurisprudência para Claude, ChatGPT e agentes de IA

Busca de jurisprudência, acórdãos, decisões e súmulas, em fontes públicas indexadas (STF, STJ, TST, TJs e Jusbrasil), por termo ou tese, com título, trecho e link. Hospedado pela plataforma; sem credencial do usuário.

- 📊 **2 ferramentas**
- 🔒 **Somente leitura**
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Login via magic-link (sem senha)**

[English version](README.en.md) · [Documentação completa](docs/) · [Skill pra agentes](skills/)

---

## Instalar em 1 clique

### Claude (Web e Desktop)

A Anthropic unificou a instalação de MCPs em `claude.ai/customize/connectors`. **O mesmo link serve pra Claude Web e Claude Desktop** (basta estar logado):

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

**Manual** (se o deeplink não abrir): [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → cole **Nome** `Jurisprudência` e **URL** `https://api.mcp.ai/p_jurisprudencia`.

### Cursor

[➕ Instalar Jurisprudência no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=jurisprudencia&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9qdXJpc3BydWRlbmNpYSJ9)

### VS Code (Copilot Chat)

[➕ Instalar Jurisprudência no VS Code](vscode:mcp/install?name=jurisprudencia&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_jurisprudencia%22%7D)

### ChatGPT, Manus, OpenClaw e mais 40+ clientes

Funciona em qualquer cliente MCP que suporte **MCP over HTTP**. A URL do servidor é sempre:

```
https://api.mcp.ai/p_jurisprudencia
```

Detalhes por cliente: [INSTALL.md](INSTALL.md).

---

## Exemplos de uso

```
Jurisprudência sobre dano moral por negativação indevida
Tem súmula sobre prazo prescricional de cobrança?
Acórdãos recentes sobre guarda compartilhada
```

---

## 2 ferramentas disponíveis

| Tool | Descrição |
|---|---|
| `jurisprudencia_buscar` | Busca jurisprudência (acórdãos, súmulas, OJs) no acervo público LexML por termo/tese — cobre tribunais superiores e demais. |
| `jurisprudencia_sumulas` | Busca SÚMULAS (incluindo vinculantes) por termo no acervo LexML. |

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)

---

## Preços

Grátis.

---

## Privacidade & LGPD

- **Somente leitura**, nenhuma ferramenta altera dados na origem.
- **Sub-processadores**: Serper (Google Search), o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills — tudo MIT.

**Posso usar com agente próprio (não Claude/Cursor)?**
Sim — qualquer cliente que suporte MCP over HTTP. URL: `https://api.mcp.ai/p_jurisprudencia`.


---

## Suporte

- 📧 [jurisprudencia@mcp.ai](mailto:jurisprudencia@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/jurisprudencia-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_jurisprudencia` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
