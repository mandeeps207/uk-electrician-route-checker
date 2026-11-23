# UK Electrician Route Checker

A Cursor/Agent Plugin for understanding UK electrician qualification and workplace progression, published by **Elec Training Ltd**.

## What it does

The plugin connects your agent to the existing Electrician Route Checker MCP to help with:

- Planning likely next steps from existing qualifications and electrical work experience.
- Understanding Level 2, technical Level 3 and 18th Edition training.
- Understanding workplace-based Level 3 NVQ progression and evidence.
- Explaining external AM2 assessment and the conditional pathway towards an appropriate ECS Gold Card.
- Comparing adult training and apprenticeship routes where relevant.

For most adult beginners, the high-level route is Level 2 -> Level 3 -> 18th Edition where needed -> workplace-based Level 3 NVQ -> external AM2 -> appropriate ECS Gold Card eligibility. Workplace learning can overlap with study. Level 2 alone does not make someone fully qualified, and technical Level 3 classroom training alone does not demonstrate occupational competence.

This is educational guidance, mainly for the adult installation pathway in England. Requirements vary across UK nations, occupations, recognised prior learning and assessment routes. Confirm current qualification, NET assessment and ECS requirements with the relevant bodies. The plugin does not assess competence or confirm card eligibility.

## Installation

Use a client that supports the [Agent Plugins standard](https://agent-plugins.org/) and install this repository through that client's plugin installer:

```text
https://github.com/mandeeps207/uk-electrician-route-checker
```

The package has a root `plugin.json`, `mcp.json` and three discoverable skills. Client installation interfaces and supported components vary. Review the remote MCP connection before enabling it. No API key is required.

A separate `.cursor-plugin/plugin.json` provides Cursor-format metadata, including the human-readable display name, for clients and directories that use that discovery path. The root Agent Plugins manifest remains schema-conformant; both manifests identify the same plugin and use the same MCP configuration and skills.

## Included skills

| Skill | Purpose |
| --- | --- |
| [electrician-route-planning](skills/electrician-route-planning/SKILL.md) | Choose a likely route from qualifications, experience and starting point. |
| [nvq-progression](skills/nvq-progression/SKILL.md) | Understand workplace experience, evidence and NVQ progression. |
| [qualification-explainer](skills/qualification-explainer/SKILL.md) | Explain individual stages and how they fit together. |

## MCP server

The plugin uses the existing production Electrician Route Checker service over HTTPS with Streamable HTTP:

```text
https://elec-electrician-route-checker.vercel.app/mcp
```

Available tools are `get_electrician_route`, `explain_electrical_stage`, `check_nvq_progression` and `compare_electrician_routes`. Clients should discover the current tool schemas before use. This repository contains the public wrapper and skill instructions; the service is hosted separately.

Tool calls send broad qualification and experience categories to the remote service. Do not send personal details, learner documents or employer records. See the publisher's [privacy policy](https://elec.training/privacy-policy/) for provider privacy information.

## Example prompts

- I'm 35 with no electrical qualifications. What route should I take to become an electrician in the UK?
- I've completed Level 3 but have no workplace experience. What should I do next?
- Do I need an NVQ before AM2?
- Can I become an electrician without an apprenticeship?

## Publisher

[Elec Training Ltd](https://elec.training/) is a UK-wide electrical training provider for adult learners and career changers, headquartered in Birmingham.

Bank House, 8 Cherry Street, Birmingham, B2 5AL, United Kingdom.

Email: enquiry@elec.training. Phone: 0330 822 5337.

Elec Training does not offer apprenticeships or deliver AM2. AM2 is completed externally at an approved NET assessment centre.

## Licence

[MIT](LICENSE). The licence covers this repository's wrapper and skills; it does not grant rights to the separately hosted service or third-party trademarks.
