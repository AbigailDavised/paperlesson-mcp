

[![mcptry](https://mcptry.com/badge/com.paperlesson/mcp)](https://mcptry.com/servers/com.paperlesson/mcp)

[![Official Website](https://img.shields.io/badge/Website-paperlesson.com-blue)](https://paperlesson.com)
[![MCP Registry](https://img.shields.io/badge/MCP_Registry-com.paperlesson%2Fmcp-green)](https://www.mcptry.com/servers/com.paperlesson/mcp)
[![Glama Connector](https://img.shields.io/badge/Glama-Connector-purple)](https://glama.ai/mcp/connectors/com.paperlesson/mcp)

Generate seeded K-12 math drills with answer keys, handwriting ruling specs & vector PDFs.

- **Official Workbench**: [https://paperlesson.com](https://paperlesson.com)
- **Remote MCP Endpoint**: `https://paperlesson.com/api/mcp` (`streamable-http`, read-only, no API key required)
- **Public OpenAPI 3.0**: [https://paperlesson.com/openapi.json](https://paperlesson.com/openapi.json)
- **LLM Context**: [https://paperlesson.com/llms.txt](https://paperlesson.com/llms.txt) · [https://paperlesson.com/llms-full.txt](https://paperlesson.com/llms-full.txt)

## Tools Provided (8 Read-Only Tools)

| Tool Name | Summary |
| :--- | :--- |
| `generate_seeded_math_drill_set` | Generate a reproducible set of K-12 arithmetic, fraction, or order-of-operations practice problems with exact answer keys using deterministic mulberry32 PRNG. |
| `lookup_handwriting_ruling_specs` | Look up exact physical millimeter and PostScript point (72 pt/inch) baseline, midline (x-height), and descender spacing for Pre-K through Grade 5 handwriting paper. |
| `build_name_tracing_worksheet_config` | Configure custom student name tracing repetition rows, progressive fade-out scaffolding (solid guide -> dashed trace -> independent baseline), and paper orientation. |
| `lookup_cursive_stroke_group_progression` | Retrieve the optimal stroke-family teaching order for cursive lowercase and uppercase letters (undercurve, downcurve, overcurve, slant connectors) rather than alphabetical order. |
| `generate_fraction_number_line_coordinates` | Compute exact vector tick coordinates and benchmark labels for teaching proper fractions, improper fractions, and equivalent fractions on a 0-to-1 or 0-to-2 number line. |
| `explain_order_of_operations_step_tree` | Break down multi-step arithmetic expressions with parentheses, exponents, multiplication/division, and addition/subtraction for Grade 5-6 worksheet answer keys. |
| `calculate_us_letter_vs_a4_printable_margins` | Calculate exact PostScript vector coordinates (pt) and safe classroom printer margins (0.5 in / 12.7 mm) to prevent edge clipping across US Letter and ISO A4. |
| `list_paperlesson_printable_generators` | List all free true-vector PDF worksheet generators on PaperLesson with direct pre-configured landing URLs. |

## Connect in 10 Seconds

### Claude Code
```bash
claude mcp add --transport http paperlesson https://paperlesson.com/api/mcp
```

### Cursor / Claude Desktop / Windsurf (`mcp.json`)
```json
{
  "mcpServers": {
    "paperlesson": {
      "type": "streamable-http",
      "url": "https://paperlesson.com/api/mcp"
    }
  }
}
```

### Agent Skill (`skills.sh`)
```bash
npx -y skills@latest add AbigailDavised/paperlesson-mcp -y
```

## License

MIT © [PaperLesson](https://paperlesson.com)
