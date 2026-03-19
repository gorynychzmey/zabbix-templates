# Anthropic Admin API Usage & Cost Template

Zabbix template for monitoring Anthropic organization usage and cost through the Anthropic Admin API.

## What it monitors

- uncached input tokens
- cache creation input tokens
- cache read input tokens
- output tokens
- total input tokens
- total tokens
- hourly cost
- daily cumulative spend
- monthly cumulative spend

## Requirements

- Zabbix 7.x
- Anthropic organization access
- Anthropic Admin API key

## Files

- `template_anthropic_admin_api_zabbix_7.yaml` — Zabbix export template

## Setup

1. Import the YAML template into Zabbix
2. Link it to a host
3. Set required host or template macros
4. Store the Admin API key securely
5. Validate that data is being collected

## Required macros

- `{$ANTHROPIC.ADMIN.API.KEY}` — Anthropic Admin API key

Optional threshold macros can be adjusted depending on your environment and spend profile.

## Notes

- Usage and cost data from Anthropic may appear with a short delay
- Cost values are derived from the Anthropic cost report API response
- This template is intended for organization-level observability, not individual end-user accounting

## License

MIT
