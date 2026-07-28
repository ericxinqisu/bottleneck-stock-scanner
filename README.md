# Bottleneck Stock Scanner

A reusable AI agent skill for finding public companies positioned around hard-to-scale supply-chain bottlenecks.

Instead of chasing popular stocks, the scanner starts with a fast-growing demand trend—such as AI infrastructure, semiconductors, power, critical minerals, cybersecurity, defense, or healthcare—and asks:

> If this industry keeps growing, which company could become difficult to avoid?

The skill selects one company per theme, checks recent supporting evidence, identifies what investors should monitor, and clearly explains the major risks.

## What It Does

- Finds companies connected to scarce or difficult-to-scale capabilities.
- Uses one stock per supply-chain theme to reduce hidden concentration.
- Requires recent evidence such as orders, backlog, customer agreements, regulatory approvals, or financial results.
- Assigns a clear risk level to every candidate.
- Produces a structured, source-backed research report.
- Avoids price targets, entry prices, position sizing, and buy or sell recommendations.

> **Important:** This skill is for research and educational purposes only. It is not financial advice.

## Download

Go to the [latest GitHub Release](https://github.com/MerryRanger922/bottleneck-stock-scanner/releases/latest) and download:

```text
bottleneck-stock-scanner.skill
```

You can also use the [direct download link](https://github.com/MerryRanger922/bottleneck-stock-scanner/releases/latest/download/bottleneck-stock-scanner.skill).

## Install in ChatGPT Desktop

1. Download `bottleneck-stock-scanner.skill` from the latest Release.
2. Open the ChatGPT desktop app.
3. Open **Skills** in the sidebar or profile menu.
4. Select **New Skill → Upload from your computer**.
5. Choose the downloaded `.skill` file.
6. Start a new chat and ask ChatGPT to use the skill.

If your version supports installation from a conversation, attach the file and say:

```text
Install this skill and make it available in future chats.
```

If ChatGPT treats it only as a normal attachment, use the **Skills** menu instead.

## Install in Claude or Claude Desktop

Claude accepts custom skills as ZIP packages. The downloaded `.skill` file is a ZIP-based skill package.

1. Download `bottleneck-stock-scanner.skill`.
2. Open Claude or Claude Desktop.
3. Go to **Customize → Skills**.
4. Select **+ → Create skill → Upload a skill**.
5. Upload the package and enable the skill.

If Claude does not accept the `.skill` extension, make a copy, rename it to `bottleneck-stock-scanner.zip`, and upload the renamed ZIP file.

If your version supports installation from a conversation, attach the `.skill` or ZIP file and say:

```text
Install this skill and make it available in future chats.
```

## Install with a CLI Agent

Download the package and give its location to your CLI agent with this prompt:

```text
Install the skill package at /path/to/bottleneck-stock-scanner.skill as a global user skill for this CLI agent.

Inspect the archive first and verify that it contains a valid SKILL.md. Install it in this agent's official global user-skills directory so it is available across all projects. Do not overwrite an existing version without asking. After installation, verify that the skill is discoverable and tell me the exact installation path. If this CLI does not support Agent Skills, tell me instead of inventing a location.
```

There is no single skills folder shared by every CLI agent. Each agent has its own location.

### Codex CLI

Install globally for all Codex projects:

```bash
mkdir -p ~/.agents/skills
unzip /path/to/bottleneck-stock-scanner.skill -d ~/.agents/skills
```

Then restart Codex if needed and run `/skills`. Invoke it directly with `$bottleneck-stock-scanner`.

For one repository only, extract it into `YOUR-REPOSITORY/.agents/skills/`.

### Claude Code

Install globally for all Claude Code projects:

```bash
mkdir -p ~/.claude/skills
unzip /path/to/bottleneck-stock-scanner.skill -d ~/.claude/skills
```

Then run `/skills`. Invoke it directly with `/bottleneck-stock-scanner`.

For one repository only, extract it into `YOUR-REPOSITORY/.claude/skills/`.

### Other CLI Agents

This package follows the open Agent Skills structure: a skill folder containing a `SKILL.md` file. Check the agent's documentation for its global skills directory, extract the package there, and restart the agent if necessary. Not every AI CLI supports Agent Skills.

## Example Prompts

```text
Run a bottleneck stock scan using the default settings.
```

```text
Find 10 U.S.-listed companies across 10 different supply-chain bottleneck themes using current primary sources.
```

## Safety Notes

- Review any skill before installing it, especially if it contains scripts.
- This skill does not place trades or access brokerage accounts.
- Live research requires internet or web-search access.
- The generated watchlist is a research starting point, not a list of recommendations.

## Official References

- [OpenAI: Build and install skills](https://learn.chatgpt.com/docs/build-skills)
- [Anthropic: Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude)
- [Anthropic: Extend Claude Code with skills](https://code.claude.com/docs/en/slash-commands)
- [Agent Skills open standard](https://agentskills.io)
