# mcp-deliverability

MCP server for email deliverability optimization - check deliverability, track IP reputation, analyze bounces.

## Tools

### check_deliverability
Check email deliverability for a domain or IP.

**Parameters:**
- `target` (string, required): Domain or IP address to check
- `type` (string, optional): "domain" or "ip" (default: "domain")

### track_ip_reputation
Track IP reputation over time.

**Parameters:**
- `ip` (string, required): IP address to track
- `days` (integer, optional): Days of history (default: 30)

### analyze_bounces
Analyze bounce patterns and identify issues.

**Parameters:**
- `campaign_id` (string, optional): Campaign identifier (optional, analyzes all if not provided)
- `days` (integer, optional): Days of bounce history to analyze (default: 30)

## Installation

```bash
pip install -r requirements.txt
```

## Usage

```bash
python main.py
```

## Connecting to Claude Desktop

Add to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "deliverability": {
      "command": "python",
      "args": ["/path/to/mcp-deliverability/main.py"],
      "cwd": "/path/to/mcp-deliverability"
    }
  }
}
```

## License

MIT