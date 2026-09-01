# Jurisprudência

### Case law from 17 Brazilian courts for Claude, Cursor and AI agents

Brazilian case law search across 17 courts: the Supreme Court, the Superior Courts, federal appellate courts, the federal tax council and eleven state courts. Every decision comes with the judging body, rapporteur, date, the exact snippet that matched your query and the link to the official site. Free, no login, hosted by the platform.

- ⚖️ **17 courts**: Supreme Court, Superior Courts, federal appellate courts, the federal tax council and eleven state courts
- 🎯 **The snippet that actually MATCHED**, not the boilerplate opening every ruling shares
- 🔗 **Link to the court's official site** on every result, so anything can be verified
- 📄 **Full text on demand** where the ruling allows it, flagged per record
- 🚦 **Says when it does not know**: an unavailable source or outdated records become an explicit notice, never an unexplained blank
- ⚠️ **Flags what does not bind a judge**: administrative council rulings are marked as such
- 🔒 **Read-only**
- ⚡ **Free, no login, no credentials**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue

[Versão em português](README.md) · [Full docs (PT-BR)](docs/) · [Agent skill](skills/)

---

## One-click install

### Claude (Web and Desktop)

Anthropic unified MCP installation at `claude.ai/customize/connectors`. **The same link works for Claude Web and Claude Desktop** (just be logged in):

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

**Manual** (if the deeplink does not open): [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → paste **Name** `Jurisprudência` and **URL** `https://api.mcp.ai/p_jurisprudencia`.

### Cursor

[➕ Install Jurisprudência in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=jurisprudencia&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9qdXJpc3BydWRlbmNpYSJ9)

### VS Code (Copilot Chat)

[➕ Install Jurisprudência in VS Code](vscode:mcp/install?name=jurisprudencia&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_jurisprudencia%22%7D)

### ChatGPT, Manus, OpenClaw and 40+ other clients

Works with any MCP client that speaks **MCP over HTTP**. The server URL is always:

```
https://api.mcp.ai/p_jurisprudencia
```

Per-client details: [INSTALL.md](INSTALL.md).

---

## Example prompts

```
Case law on moral damages for workplace harassment
What has the Superior Court decided on statute of limitations for condo fees?
Is there a binding precedent on dismissal for job abandonment?
Search São Paulo and Rio state courts for adverse possession rulings and compare
Read the full text of the ruling you found and summarise the holding
```

---

## 3 tools available

| Tool | Description |
|---|---|
| `jurisprudencia_buscar` | Busca jurisprudência (acórdãos, súmulas, orientações jurisprudenciais, temas) por termo ou tese. |
| `jurisprudencia_sumulas` | Busca SÚMULAS (incluindo vinculantes) por termo. |
| `jurisprudencia_documento` | Lê o INTEIRO TEOR de uma decisão (texto completo do acórdão, não o resumo). |

Details for each tool: [docs/ferramentas.md](docs/ferramentas.md) (PT-BR)


---

## Como funciona

```
1. Instala o MCP no seu cliente (Claude / Cursor / VS Code)
2. Pergunta em português comum, sem sintaxe de portal de tribunal
3. jurisprudencia_buscar devolve as decisões com o trecho que casou e o link
4. jurisprudencia_sumulas restringe a súmulas e enunciados
5. jurisprudencia_documento lê o inteiro teor de uma decisão que você escolheu
```

Restrinja por tribunal quando souber onde procurar (`tribunais: ["STJ", "TJSP"]`),
ou deixe a busca ampla. No termo funcionam os operadores de sempre: espaço é E,
"entre aspas" é frase exata, OR é ou, e `-palavra` exclui.

### O que a resposta garante

Campo nulo é ausência de informação na fonte, não defeito: nem toda publicação
permite afirmar relator, órgão ou numeração, e inventar seria pior. Quando o
inteiro teor pode ser lido, o registro diz isso em `texto_integral_disponivel`.
E zero resultado nunca chega sozinho: vem com o motivo e o que tentar em seguida,
porque "não achei" e "não existe" são coisas diferentes num parecer.

Combina com o **DataJud MCP** (processo pelo número do CNJ) e o **Legal MCP**
(raio-X consolidado de uma parte) para pesquisa jurídica de ponta a ponta.

---

## Pricing

Free.

---

## Privacy & data protection

- **Read-only**, no tool changes data at the source.
- **Sub-processors**: Serper (Google Search), the LLM host you choose (Claude, ChatGPT, Cursor, your own agent). Full list in [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Data returned by the tools is sent to **the LLM host you choose**, a sub-processor outside our control. We recommend plans with training opt-out.

---

## FAQ

**Quais tribunais estão cobertos?**
Dezessete: STF, STJ e TST; TRF3 e TRF4; o CARF; e os tribunais de justiça de São Paulo, Rio de Janeiro, Minas Gerais, Rio Grande do Sul, Paraná, Santa Catarina, Ceará, Goiás, Mato Grosso, Mato Grosso do Sul e Maranhão.

**Os resultados são atuais?**
A consulta alcança o que o tribunal tem publicado, e não um recorte com data de corte. Quando um tribunal específico está com o acervo atrasado, a própria resposta avisa, com a data mais recente que ela encontrou, para você não tratar uma decisão antiga como o estado atual da jurisprudência.

**Precisa de login, cadastro ou certificado?**
Não. É grátis e sem credencial. Você não precisa de conta em nenhum tribunal.

**Serve para citar em petição?**
Serve para encontrar e ler. Todo resultado traz o link no site oficial do tribunal, e a conferência lá é obrigatória antes de citar. Decisão de conselho administrativo vem marcada, porque vincula a administração e não o juiz.

**Por que uma busca voltou vazia?**
Quase sempre é vocabulário: o tribunal nomeia a tese de um jeito diferente do coloquial. A resposta sugere o que tentar. Se a fonte estiver indisponível no momento, ela diz isso explicitamente, o que é diferente de a decisão não existir.

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills, tudo MIT.


---

## Support

- 📧 [jurisprudencia@mcp.ai](mailto:jurisprudencia@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/jurisprudencia-mcp/issues)
- 📄 [docs/](docs/)

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_jurisprudencia` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
