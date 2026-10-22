# Speed Workspace — demo visual

Demo React + TypeScript para modernização do painel Speed Fibra: temas claro/escuro, layout responsivo, indicadores, gráficos, tabelas, filas e modais.

## Executar
Requisitos: Node.js 22 ou superior e npm.

```sh
npm ci
npm run dev
```

Para produção: `npm run build`. Para servir o build: `npm run preview`.
Se o cache padrão não for gravável: `npm ci --cache /tmp/speed-cache`.

## Funcionalidades demonstradas
- Painel, indicadores, distribuição de filas, gráfico por hora e equipe por setor.
- Tema com preferência persistida no navegador; navegação mobile.
- Busca de agentes e filtro por setor.
- Modal de filas: nome atualizado na sessão; demais campos ilustram o formulário.
- Discador, pausa e encaminhamento simulados.
- Relatórios ilustrativos e exportação CSV dos dados de filas.
- Feriados: inclusão e remoção na sessão.

Os números são amostras dos prints e registros ilustrativos. Os recortes de filas e dashboard são diferentes e não devem ser somados como um único período. Horários e estados não refletem uma operação real. Filtros de período demonstram estados visuais, sem recalcular a amostra. Apenas o tema persiste após recarregar. O CSV sempre exporta filas.

Campanhas, ramais, troncos, URA, monitor, segurança e backups são áreas reservadas para integração. Não há backend, autenticação, API de clientes ou telefonia real.

## Integrar ao seu sistema
1. Reutilize os tokens e componentes visuais de `src/style.css` e `src/main.tsx`.
2. Separe App em Sidebar, Topbar, AgentBar, StatCard, QueueTable, QueueModal e páginas.
3. Substitua `initialQueues`, `agents` e `hourly` pelos dados da API existente.
4. Preserve autenticação, permissões, campos e regras de negócio do projeto original.
5. Conecte formulários, filtros, chamadas e ações aos serviços reais.
6. Substitua a marca tipográfica pelo SVG oficial; adicione estados de carregamento, erros e confirmações para ações destrutivas.

As fontes opcionais DM Sans e Manrope usam Google Fonts, com fallback local. Ícones e gráficos estão no bundle. Esta versão foi reconstruída a partir da conversa após a troca do ambiente de execução; não é uma cópia binária do ZIP anterior.
