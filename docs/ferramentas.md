# Ferramentas

Jurisprudência expõe 3 ferramentas (todas somente leitura).

### 1. `jurisprudencia_buscar`
**Input**: `termo`, `tipo` (opcional), `tribunais` (opcional), `data_de` (opcional), `data_ate` (opcional), `ordenar` (opcional), `max` (opcional)

Busca jurisprudência (acórdãos, súmulas, orientações jurisprudenciais, temas) por termo ou tese.

### 2. `jurisprudencia_sumulas`
**Input**: `termo`, `max` (opcional)

Busca SÚMULAS (incluindo vinculantes) por termo.

### 3. `jurisprudencia_documento`
**Input**: `id` (opcional), `numeracao` (opcional), `tribunal` (opcional), `ids` (opcional)

Lê o INTEIRO TEOR de uma decisão (texto completo do acórdão, não o resumo).

## Prompts de exemplo

```
O que o STJ decidiu sobre prazo prescricional em cobrança de condomínio?
Busque no TJSP e no TJRJ decisões sobre usucapião extraordinário e compare
Jurisprudência sobre dano moral por inscrição indevida em cadastro de inadimplentes
Tem súmula do TST sobre justa causa por abandono de emprego?
Leia o inteiro teor do acórdão que você achou e resuma a tese
```
