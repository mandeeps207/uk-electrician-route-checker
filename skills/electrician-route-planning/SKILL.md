---
name: electrician-route-planning
description: Plan a UK electrician qualification route based on the user's current qualifications, electrical experience and career starting point.
---

# Electrician route planning

Use the Electrician Route Checker MCP for complete beginners, career changers, learners who have completed Level 2 or Level 3, experienced electrical workers, and people unsure of their next stage.

Ask for the UK nation, current qualifications, broad electrical work experience and whether the user currently does suitable electrical work when those facts are missing and affect the route. Clarify whether a Level 3 award is a technical diploma or a workplace competence qualification. Do not request names, contact details, employer details or learner documents.

Discover the connected `electrician-route-checker` server's tools and inspect their current input schemas. Call `get_electrician_route` using supported enum values and facts the user supplied. Do not infer no qualifications or no experience from silence. Use an explicit unknown value where the schema supports it; otherwise ask for the missing fact. For apprenticeship versus adult-training comparisons, call `compare_electrician_routes` with the relevant supported routes.

Explain the returned likely next step and why it fits the user's starting point. For most adult beginners, describe Level 2 -> Level 3 -> 18th Edition where needed -> workplace-based Level 3 NVQ -> external AM2 -> appropriate ECS Gold Card eligibility. Suitable electrical work and workplace learning are needed for competence assessment and can overlap with study. Existing recognised qualifications may change the route.

Preserve these distinctions:

- Level 2 alone does not make someone fully qualified. Level 3 classroom training alone does not establish occupational competence.
- Elec Training does not offer apprenticeships or deliver AM2. AM2 takes place externally at an approved NET assessment centre; the relevant assessment variant depends on the route.
- An ECS Gold Card is conditional on the relevant current ECS requirements. Do not promise eligibility, employment, an assessment pass or a completion date.
- Routes vary by UK nation and occupation. State the tool's jurisdictional limits and refer uncertain eligibility questions to the relevant awarding body, NET or ECS.

Keep advice educational. Include provider information only when relevant to the question. If the MCP is unavailable, explain that personalised route guidance could not be verified and suggest retrying; do not fabricate a tool result or recreate the qualification engine.
