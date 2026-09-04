# Demo 01 - Agent Chaining: Weekly Well Manifest

Classification: Public

This demo uses a fictional Microsoft Fake Company created for demonstration purposes. Any resemblance to real organizations, people, products, services, or data is coincidental. Do not use customer confidential information in this package.

## Scenario

Trey Research receives three weekly Excel workbooks with oil and gas well-test results across Texas, New Mexico, Oklahoma, Louisiana, and Arkansas. The presenter uses Microsoft 365 Copilot Chat as the starting experience, attaches the right agents as the work evolves, and turns fragmented well-test data into a weekly manifest, a stylized Well Brief, a PowerPoint rundown, and a meeting agenda.

## Demo Tool

Microsoft 365 Copilot Chat with the Analyst agent, Excel agent, Word agent, and PowerPoint agent. This is a use-focused agent chaining demo: the presenter attaches agents at each handoff rather than building a new agent.

## Files to Attach

- [`Well_Test_Results_Southwest.xlsx`](https://github.com/AndrewConniff/oil-gas-wells/blob/main/demo/sample-data/Well_Test_Results_Southwest.xlsx)
- [`Well_Test_Results_Midcontinent.xlsx`](https://github.com/AndrewConniff/oil-gas-wells/blob/main/demo/sample-data/Well_Test_Results_Midcontinent.xlsx)
- [`Well_Test_Results_Gulf_ArkLaTex.xlsx`](https://github.com/AndrewConniff/oil-gas-wells/blob/main/demo/sample-data/Well_Test_Results_Gulf_ArkLaTex.xlsx)
- [`Manifest_Template.xlsx`](https://github.com/AndrewConniff/oil-gas-wells/blob/main/demo/sample-data/Manifest_Template.xlsx)
- [`Well Brief Template.docx`](https://github.com/AndrewConniff/oil-gas-wells/blob/main/demo/sample-data/Well%20Brief%20Template.docx)
- [`Executive_Rundown_Template.pptx`](https://github.com/AndrewConniff/oil-gas-wells/blob/main/demo/sample-data/Executive_Rundown_Template.pptx)

## Prompts

### Prompt 1 - Analyst agent: combine and analyze the three incoming well files

**Agent:** Analyst agent

**Sources/files used:** `Well_Test_Results_Southwest.xlsx`, `Well_Test_Results_Midcontinent.xlsx`, `Well_Test_Results_Gulf_ArkLaTex.xlsx`

**Exact prompt text:**

> You are my oil and gas operations analyst. I attached three weekly well-result workbooks. Combine the Well Tests and Mineral Assay sheets across all files, ignore Weather Field Conditions and Land Rights unless they explain an anomaly, and produce a weekly operating analysis for Trey Research. Show all-up numbers by state and by area, include latitude and longitude coverage, call out mineral indicators such as lithium, bromide, chloride, silica, H2S, CO2, produced-water TDS, API gravity, gas BTU, pressure, and EUR. Include graphics: a state production comparison, an area-level mineral uplift view, a risk summary, and a map visual using latitude and longitude. End with the exact data points that should be carried into a weekly manifest.

**Required result format:**

A concise business response with structured rollups, named outputs, and visuals appropriate to the active agent.

**Acceptance criteria:**

Response includes combined totals across all three files, state and area rollups, at least three visuals or visual specifications, and a map visual based on latitude/longitude.

**Next handoff:**

Add the Excel agent and attach Manifest_Template.xlsx.

**Failure behavior:**

If Copilot includes irrelevant source details, ask it to revise using only manifest-ready analysis and to keep weather, land-rights, and lease details out of the output except as summarized risk rationale.

### Prompt 2 - Excel agent: create the weekly manifest workbook

**Agent:** Excel agent

**Sources/files used:** `Manifest_Template.xlsx`

**Exact prompt text:**

> Using Manifest_Template.xlsx as the structure, create a new weekly manifest workbook from the analysis already in this chat. Include only the analysis results needed for the manifest: all-up production and mineral numbers by state and area, a location table with latitude and longitude, risk flags, recommended actions, and a map visual. Do not include weather details, land-rights records, lease notes, or other source-system context unless they are summarized as a risk explanation. Name the new workbook Weekly_Well_Manifest_2026-09-04.xlsx and preserve the template's modern corporate formatting.

**Required result format:**

A concise business response with structured rollups, named outputs, and visuals appropriate to the active agent.

**Acceptance criteria:**

New workbook follows the template, contains State Rollup, Area Rollup, Location Map, Visuals, and Data Dictionary content, and excludes raw weather and land-rights details.

**Next handoff:**

Add the Word agent and attach Well Brief Template.docx.

**Failure behavior:**

If Copilot includes irrelevant source details, ask it to revise using only manifest-ready analysis and to keep weather, land-rights, and lease details out of the output except as summarized risk rationale.

### Prompt 3 - Word agent: create the stylized well brief

**Agent:** Word agent

**Sources/files used:** `Well Brief Template.docx`

**Exact prompt text:**

> Using Well Brief Template.docx, create a polished weekly Well Brief from the chat so far and the new manifest details. Keep the design highly stylized and executive-ready. Include an executive summary, state and area highlights, map narrative, mineral opportunity notes, production-risk signals, recommended operating actions, and a concise appendix of the key figures. Name the document Weekly_Well_Brief_2026-09-04.docx.

**Required result format:**

A concise business response with structured rollups, named outputs, and visuals appropriate to the active agent.

**Acceptance criteria:**

Brief is executive-ready, visually styled, and uses the manifest analysis without copying unnecessary source-system fields.

**Next handoff:**

Add the PowerPoint agent and attach Executive_Rundown_Template.pptx.

**Failure behavior:**

If Copilot includes irrelevant source details, ask it to revise using only manifest-ready analysis and to keep weather, land-rights, and lease details out of the output except as summarized risk rationale.

### Prompt 4 - PowerPoint agent: create the executive rundown deck

**Agent:** PowerPoint agent

**Sources/files used:** `Executive_Rundown_Template.pptx`

**Exact prompt text:**

> Using Executive_Rundown_Template.pptx as the style reference, create a short executive rundown deck from the chat, manifest, and Well Brief. Use the same modern corporate visual style. Include title, weekly operating thesis, state rollup, area and mineral signals, map visual slide, risk and action slide, and meeting discussion slide. Name the deck Weekly_Well_Rundown_2026-09-04.pptx.

**Required result format:**

A concise business response with structured rollups, named outputs, and visuals appropriate to the active agent.

**Acceptance criteria:**

Deck uses the provided style, includes visual slides rather than plain bullets, and tells a concise story from source files to actions.

**Next handoff:**

Ask Copilot for the meeting email and agenda.

**Failure behavior:**

If Copilot includes irrelevant source details, ask it to revise using only manifest-ready analysis and to keep weather, land-rights, and lease details out of the output except as summarized risk rationale.

### Prompt 5 - Copilot Chat: draft meeting email and agenda

**Agent:** Microsoft 365 Copilot Chat

**Sources/files used:** Chat context and generated outputs from the previous steps.

**Exact prompt text:**

> Draft a brief meeting invite email and agenda for the weekly well manifest review. Keep it concise, executive-ready, and focused on the generated manifest, Well Brief, and rundown deck. Include a 30-minute agenda with opening context, state and area results, map and mineral signals, risk decisions, and next actions. Do not include raw weather, land-rights, or lease details.

**Required result format:**

A concise business response with structured rollups, named outputs, and visuals appropriate to the active agent.

**Acceptance criteria:**

Email is brief, agenda is time-boxed, and it references the outputs created in the agent chain.

**Next handoff:**

Presenter sends or adapts the invite in Outlook.

**Failure behavior:**

If Copilot includes irrelevant source details, ask it to revise using only manifest-ready analysis and to keep weather, land-rights, and lease details out of the output except as summarized risk rationale.

## Test and Validate

Before class, run the prompts once in a fresh Copilot Chat. Confirm the first response combines all three workbooks, the manifest excludes unneeded source-system details, and the final Word and PowerPoint outputs retain the shared copper, petrol, sage, and sand visual style.

## Cleanup

Remove generated class-run outputs from the chat after the session if they are no longer needed. Keep the source package files available for reuse.
