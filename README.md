# Bottleneck Stock Scanner V2

A reusable AI research skill for finding public companies positioned around supply-chain bottlenecks—and testing whether each bottleneck is likely temporary or genuinely difficult to scale.

Instead of starting with popular stocks, the scanner starts with a growing demand wave, maps the required supply chain, identifies the binding constraint, and asks:

> If this industry keeps growing, which company could become difficult to avoid—and will the constraint last long enough for the company to capture value?

## What V2 Adds

Every stock now receives one required durability indicator:

- **Probably Temporary**
- **Potentially Hard to Scale**

Each classification includes:

- Confidence level
- Research horizon
- Demand, qualified-supply, and workaround timelines
- Evidence supporting and challenging the conclusion
- Company value-capture analysis
- Observable conditions that would flip the indicator

## Research Framework

V2 evaluates every candidate using seven tests:

1. Multi-constraint supply-chain mapping
2. Money-and-time test
3. Substitution and input-intensity test
4. Entry-barrier test
5. Full-cycle historical test
6. Bottleneck-migration test
7. Company value-capture test

The methodology draws on research approaches from Epoch AI, Google DeepMind, Oaktree, Morgan Stanley Investment Management, and Baillie Gifford.

## Core Rules

- Select one stock per distinct supply-chain theme.
- Use live research and recent dated evidence.
- Require a primary company source and an independent source.
- Search for disconfirming evidence—not only support for the thesis.
- Distinguish announced capacity from customer-qualified output.
- Separate an industry bottleneck from the company’s ability to capture value.
- Assign an explicit risk level to every candidate.
- Avoid price targets, entry prices, position sizing, and buy or sell recommendations.

## Report Output

The normal deliverable is a source-backed PDF containing:

- Research disclaimer
- Executive summary
- One-theme-per-stock watchlist
- Durability indicator and confidence for every stock
- Per-stock deep dives
- Counterevidence and thesis invalidation conditions
- Monitoring signals and key risks
- Dated source list with direct links

## Download

Open the [latest GitHub Release](https://github.com/MerryRanger922/bottleneck-stock-scanner/releases/latest) and download:

```text
bottleneck-stock-scanner-v2.skill
```

[Direct download from the latest release](https://github.com/MerryRanger922/bottleneck-stock-scanner/releases/latest/download/bottleneck-stock-scanner-v2.skill)

## Install

### Codex or ChatGPT Desktop

1. Download `bottleneck-stock-scanner-v2.skill`.
2. Open the Skills section in the desktop app.
3. Choose **New Skill** or **Upload from your computer**.
4. Select the downloaded `.skill` file.
5. Start a new task and ask the app to use the Bottleneck Stock Scanner.

If installation from a conversation is supported, attach the file and say:

```text
Install this skill and make it available in future chats.
```

### Claude or Claude Desktop

If your version supports reusable skills or project instructions, upload the `.skill` file or copy the included `SKILL.md` and reference file into the relevant project.

### Manual installation

The package is a ZIP-compatible archive containing:

```text
bottleneck-stock-scanner/SKILL.md
bottleneck-stock-scanner/agents/openai.yaml
bottleneck-stock-scanner/references/durability-classification.md
```

Extract the folder into the skills directory used by your AI agent environment.

## Example Prompts

```text
Use the bottleneck stock scanner to find 10 U.S.-listed candidates across 10 different supply-chain themes.
```

```text
Classify every candidate as Probably Temporary or Potentially Hard to Scale and show the evidence against each conclusion.
```

```text
Update the bottleneck report using current filings, company sources, competitors, customers, and independent research.
```

## Important Notice

This skill is for research and education only. It is not financial advice and does not provide recommendations to buy or sell securities. Small-cap and thematic stocks can be extremely volatile.
