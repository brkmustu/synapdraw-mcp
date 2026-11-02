# SynapDraw MCP Server

SynapDraw SDLC Super-App için canlı Çizim Tuvali, UI/UX Tasarım Tuvali, Görev Panosu ve TDD Test Stüdyosu orkestrasyonu sağlayan Model Context Protocol (MCP) sunucusu.

## Kurulum ve Derleme

```bash
cd synapdraw-mcp
npm install
npm run build
```

## Çalıştırma

### HTTP / Canlı SSE Köprüsü (`http://localhost:3001`)

```bash
npm run serve
```

### Claude Desktop / Gemini Antigravity Yapılandırması (`stdio`)

```json
{
  "mcpServers": {
    "synapdraw": {
      "command": "node",
      "args": ["/path/to/synapdraw/synapdraw-mcp/dist/index.js", "--stdio"]
    }
  }
}
```

## Sunulan MCP Araçları

- **Çizim & Mimari (`sketch`):** `read_me`, `render_mermaid`, `render_html`, `create_view`, `get_canvas_context`, `clear_canvas`
- **UI/UX Tasarım (`design`):** `get_canvas_type`, `render_design`, `get_design_tree`, `update_node_styles`, `export_design_code`
- **SDLC Proje, Görev & TDD Yönetimi:** `get_project_sdlc_overview`, `upsert_project_task`, `upsert_tdd_scenario`, `generate_tdd_from_task`

## Lisans

MIT
