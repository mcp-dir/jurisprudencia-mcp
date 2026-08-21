---
name: jurisprudencia-mcp
description: Skill da REST API do Jurisprudência na MCP.AI: 2 endpoints em /api/jurisprudencia. Busca de jurisprudência, acórdãos, decisões e súmulas, em fontes públicas indexadas (STF, STJ, TST, TJs e Jusbrasil), por termo ou tese, com título, trecho e link. Hospedado pela plataforma; sem credencial do usuário. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Jurisprudência — REST API skill

Você tem acesso à **Jurisprudência** REST API na MCP.AI.

> Busca de jurisprudência, acórdãos, decisões e súmulas, em fontes públicas indexadas (STF, STJ, TST, TJs e Jusbrasil), por termo ou tese, com título, trecho e link. Hospedado pela plataforma; sem credencial do usuário.

## Base URL

```
https://api.mcp.ai/api/jurisprudencia
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/jurisprudencia/buscar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"termo":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/jurisprudencia/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (2)

#### `jurisprudencia_buscar`

Busca jurisprudência (acórdãos, súmulas, OJs) no acervo público LexML por termo/tese — cobre tribunais superiores e demais. _(POST /api/jurisprudencia/buscar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `termo` | string | Sim | Termo, tese ou assunto (ex.: 'dano moral negativação indevida'). |
| `tipo` | string | Não | Filtra por tipo de documento (ex.: "Acórdão", "Súmula"). |
| `max` | integer | Não | Resultados (default 10, máx 50). |

#### `jurisprudencia_sumulas`

Busca SÚMULAS (incluindo vinculantes) por termo no acervo LexML. _(POST /api/jurisprudencia/sumulas)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `termo` | string | Sim | Termo/assunto da súmula. |
| `max` | integer | Não | Resultados (default 10). |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_jurisprudencia` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
