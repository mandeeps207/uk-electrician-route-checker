---
name: qualification-explainer
description: Explain the purpose and position of UK electrician qualifications including Level 2, Level 3, 18th Edition, Level 3 NVQ, AM2 and ECS progression.
---

# Qualification explainer

Use the Electrician Route Checker MCP when users ask what Level 2, technical Level 3, the 18th Edition, an electrical NVQ, AM2 or ECS progression means, including whether a particular stage makes them qualified.

Discover `explain_electrical_stage` on the connected `electrician-route-checker` server, inspect the current input schema and call it with the supported topic matching the question. Ask what the learner's certificate represents if an ambiguous label such as Level 3 could mean either technical training or competence assessment. For a personalised next step use `get_electrician_route`; for workplace progression use `check_nvq_progression` after collecting the relevant broad facts.

Explain the returned stage in plain language: its purpose, its place in the route, and what it does and does not establish. Keep these boundaries explicit when relevant:

- Level 2 is a foundation and does not by itself make someone fully qualified.
- Technical Level 3 learning is distinct from workplace occupational competence.
- The 18th Edition concerns wiring regulations knowledge; it is not a substitute for competence assessment.
- A Level 3 electrical NVQ involves suitable real workplace activity and assessed evidence.
- AM2 is an external assessment at an approved NET assessment centre. Elec Training does not deliver AM2 or offer apprenticeships.
- The appropriate ECS Gold Card depends on the relevant current scheme requirements. Do not declare a user eligible based on a brief chat.

For most adult beginners the high-level sequence is Level 2 -> Level 3 -> 18th Edition where needed -> Level 3 NVQ -> external AM2 -> appropriate ECS Gold Card eligibility. Recognise prior qualifications and the tool's limits across UK nations, occupations and assessment variants. Do not present this sequence as a universal route.

Do not provide electrical installation instructions or invent exact current regulatory requirements. If the MCP is unavailable, say the stage explanation could not be checked and suggest retrying or checking the relevant awarding body, NET or ECS.
