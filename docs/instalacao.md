# Instalação detalhada

SEFAZ MS: NFC-e é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_sefaz_ms_nfce`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_sefaz_ms_nfce` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_sefaz_ms_nfce` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_sefaz_ms_nfce` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.sefaz_ms_nfce` (ou `servers.sefaz_ms_nfce` no VS Code) do config do cliente e reinicie.
