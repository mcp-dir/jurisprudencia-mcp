# Jurisprudência

### Jurisprudência de 17 tribunais brasileiros para Claude, Cursor e agentes de IA

Pesquisa de jurisprudência em 17 tribunais brasileiros, do STF e dos superiores aos regionais federais, ao CARF e a onze tribunais de justiça estaduais. Cada decisão vem com órgão julgador, relator, data, o trecho exato que casou a busca e o link no site oficial. Grátis, sem login, hospedado pela plataforma.

- ⚖️ **17 tribunais**: STF, STJ, TST, TRF3, TRF4, CARF e os TJs de SP, RJ, MG, RS, PR, SC, CE, GO, MT, MS e MA
- 🎯 **O trecho que CASOU a busca**, não a abertura burocrática do acórdão ("Trata-se de agravo…" é igual em milhares de decisões)
- 🔗 **Link no site oficial** do tribunal em cada resultado, para conferência
- 📄 **Inteiro teor sob demanda** quando a decisão permite, sinalizado por registro
- 🚦 **Diz quando não sabe**: fonte indisponível ou acervo desatualizado vira aviso explícito, nunca um vazio sem explicação
- ⚠️ **Avisa o que não vincula juiz**: decisão de conselho administrativo vem marcada como tal
- 🔒 **Somente leitura**
- ⚡ **Grátis, sem login, sem credencial**
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue

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
O que o STJ decidiu sobre prazo prescricional em cobrança de condomínio?
Busque no TJSP e no TJRJ decisões sobre usucapião extraordinário e compare
Jurisprudência sobre dano moral por inscrição indevida em cadastro de inadimplentes
Tem súmula do TST sobre justa causa por abandono de emprego?
Leia o inteiro teor do acórdão que você achou e resuma a tese
```

---

## 3 ferramentas disponíveis

| Tool | Descrição |
|---|---|
| `jurisprudencia_buscar` | Busca jurisprudência (acórdãos, súmulas, orientações jurisprudenciais, temas) por termo ou tese. |
| `jurisprudencia_sumulas` | Busca SÚMULAS (incluindo vinculantes) por termo. |
| `jurisprudencia_documento` | Lê o INTEIRO TEOR de uma decisão (texto completo do acórdão, não o resumo). |

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)


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

## Preços

Grátis.

---

## Privacidade & LGPD

- **Somente leitura**, nenhuma ferramenta altera dados na origem.
- **Sub-processadores**: Serper (Google Search), o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

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

## Suporte

- 📧 [jurisprudencia@mcp.ai](mailto:jurisprudencia@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/jurisprudencia-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_jurisprudencia` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
