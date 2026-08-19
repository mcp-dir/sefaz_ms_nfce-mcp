# Instalação rápida

SEFAZ MS: NFC-e é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_sefaz_ms_nfce`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `SEFAZ MS: NFC-e` / `https://api.mcp.ai/p_sefaz_ms_nfce`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "sefaz_ms_nfce": { "type": "http", "url": "https://api.mcp.ai/p_sefaz_ms_nfce" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=sefaz_ms_nfce&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9zZWZhel9tc19uZmNlIn0=)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "sefaz_ms_nfce": { "url": "https://api.mcp.ai/p_sefaz_ms_nfce" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=sefaz_ms_nfce&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_sefaz_ms_nfce%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "sefaz_ms_nfce": { "type": "http", "url": "https://api.mcp.ai/p_sefaz_ms_nfce" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_sefaz_ms_nfce
```

Dúvidas? [sefaz_ms_nfce@mcp.ai](mailto:sefaz_ms_nfce@mcp.ai)
