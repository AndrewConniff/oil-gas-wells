# Oil and Gas Wells - Agent Chaining Demo

Classification: Public

This demo uses a fictional Microsoft Fake Company created for demonstration purposes. Any resemblance to real organizations, people, products, services, or data is coincidental. Do not use customer confidential information in this package.

## Fictional Microsoft Fake Company

Trey Research

## Scenario overview

This package supports a Copilot class demo showing agent chaining in Microsoft 365 Copilot Chat. The presenter starts with three incoming Excel workbooks for weekly oil and gas well-test results, adds the Analyst agent to combine and analyze them, then adds the Excel, Word, and PowerPoint agents to create a manifest workbook, a Well Brief, an executive rundown, and a meeting agenda.

## Target industry, persona, and audience

- Industry: Oil and gas exploration and production
- Persona: Operations analytics lead preparing a weekly well manifest review
- Audience: Copilot class attendees learning how to chain specialist agents in Chat
- Duration: 15-20 minutes

## Public research basis

The scenario uses public oil and gas vocabulary and concepts grounded in the U.S. Energy Information Administration overview of crude oil and petroleum products: https://www.eia.gov/energyexplained/oil-and-petroleum-products/

## Technology focus and prerequisites

- Microsoft 365 Copilot Chat
- Analyst agent, Excel agent, Word agent, and PowerPoint agent available to the presenter
- Ability to attach local Office files to Copilot Chat

## Repository contents

| Path | Purpose |
| --- | --- |
| `demo/DEMO-INSTRUCTIONS.md` | Presenter guide with exact prompts. |
| `demo/DEMO-INSTRUCTIONS.docx` | Word copy of the presenter guide. |
| `demo/sample-data/Well_Test_Results_Southwest.xlsx` | Incoming well-test workbook for Texas and New Mexico. |
| `demo/sample-data/Well_Test_Results_Midcontinent.xlsx` | Incoming well-test workbook for Texas and Oklahoma. |
| `demo/sample-data/Well_Test_Results_Gulf_ArkLaTex.xlsx` | Incoming well-test workbook for Texas, Louisiana, and Arkansas. |
| `demo/sample-data/Manifest_Template.xlsx` | Excel template for the generated weekly manifest. |
| `demo/sample-data/Well Brief Template.docx` | Word template for the generated Well Brief. |
| `demo/sample-data/Executive_Rundown_Template.pptx` | PowerPoint style template for the generated rundown. |

## Demo workflow summary

1. Attach the three incoming Excel files and add the Analyst agent to combine the well-test and mineral-assay data.
2. Add the Excel agent and attach `Manifest_Template.xlsx` to create the weekly manifest with state, area, location, and map-ready outputs.
3. Add the Word agent and attach `Well Brief Template.docx` to create a stylized executive Well Brief.
4. Add the PowerPoint agent and attach `Executive_Rundown_Template.pptx` to create the executive rundown deck.
5. Ask Copilot Chat to draft a brief invite email and agenda for the review meeting.

## Download links

- [`Well_Test_Results_Southwest.xlsx`](demo/sample-data/Well_Test_Results_Southwest.xlsx)
- [`Well_Test_Results_Midcontinent.xlsx`](demo/sample-data/Well_Test_Results_Midcontinent.xlsx)
- [`Well_Test_Results_Gulf_ArkLaTex.xlsx`](demo/sample-data/Well_Test_Results_Gulf_ArkLaTex.xlsx)
- [`Manifest_Template.xlsx`](demo/sample-data/Manifest_Template.xlsx)
- [`Well Brief Template.docx`](demo/sample-data/Well%20Brief%20Template.docx)
- [`Executive_Rundown_Template.pptx`](demo/sample-data/Executive_Rundown_Template.pptx)
- [`DEMO-INSTRUCTIONS.md`](demo/DEMO-INSTRUCTIONS.md)
- [`DEMO-INSTRUCTIONS.docx`](demo/DEMO-INSTRUCTIONS.docx)
- [`manifest.json`](manifest.json)
- [`AI-CONTENT-DECLARATION.md`](AI-CONTENT-DECLARATION.md)
- [`LICENSE`](LICENSE)

## Setup instructions

Download or open the files under `demo/sample-data/`. In Copilot Chat, begin with the three incoming Excel workbooks, then add each specialist agent and template at the step specified in `demo/DEMO-INSTRUCTIONS.md`.

## MIT license notice

This package is provided under the MIT License. See `LICENSE`.

## AI transparency summary

This repository contains AI-generated and human-reviewed demo content. See `AI-CONTENT-DECLARATION.md` for details.

## Name validation

Approved company names checked: 1. Approved person names checked: 6.
