# zabbix-templates

A collection of community-maintained Zabbix templates for monitoring third-party services, APIs, and custom integrations.

This repository starts with a template for monitoring **Anthropic Admin API usage and cost** from Zabbix and is intended to grow over time with additional reusable templates.

## Repository goals

- Keep templates practical and easy to deploy
- Prefer simple installation over unnecessary complexity
- Focus on real-world observability use cases
- Publish templates in a form that can be imported and adapted quickly

## Available templates

### Anthropic Admin API Usage & Cost

Monitors Anthropic organization-level API consumption through the **Admin API**.

Current capabilities include:

- input token usage
- output token usage
- cache-related token usage
- cost per interval
- cumulative daily spend
- cumulative monthly spend
- basic alerting thresholds for spend and token spikes

## Repository structure

```text
.
├── anthropic/
│   ├── README.md
│   └── template_anthropic_admin_api_zabbix_7.yaml
├── .gitignore
├── LICENSE
└── README.md
```

As more templates are added, each integration should have its own directory with:

- the exported Zabbix template
- a local README with integration-specific notes
- optional helper files or example scripts when needed

## Requirements

Requirements depend on the specific template, but in general:

- Zabbix 7.x or newer is recommended
- access credentials for the monitored system
- any required API permissions for the target platform

For the Anthropic template specifically:

- an **Anthropic Admin API key**
- an Anthropic organization with access to the Usage & Cost Admin API
- a Zabbix host to which the template can be linked

## Installation

General flow:

1. Clone this repository or download the needed template files
2. Import the template YAML into Zabbix
3. Link the template to a host
4. Configure required macros, secrets, and thresholds
5. Verify incoming data and adjust triggers as needed

Detailed setup steps should be documented in the subdirectory README for each template.

## Design principles

Templates in this repository are intended to be:

- importable without heroics
- readable enough to maintain
- opinionated where it saves time
- flexible where environments differ

The goal is not to build an academic museum of YAML, but to provide templates that are actually useful in production.

## Compatibility and support

These templates are provided as community artifacts. They may require minor adjustments depending on:

- Zabbix version
- target API changes
- authentication model
- environment-specific conventions

No guarantee is made that every template will remain compatible with every upstream API version forever.

## Contributing

Contributions are welcome.

Reasonable contributions include:

- new templates
- bug fixes
- compatibility fixes
- documentation improvements
- better defaults for triggers, preprocessing, and macros

When contributing:

- keep templates focused
- document required macros and permissions
- prefer explicit naming
- avoid hidden dependencies unless clearly documented

## License

This repository is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

## Disclaimer

This project is an independent community repository and is not affiliated with, endorsed by, or sponsored by Zabbix or Anthropic.
